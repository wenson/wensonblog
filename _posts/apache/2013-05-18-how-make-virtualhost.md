---
layout: post
title: xampp添加不同目录虚拟主机
category: apache
tags : [apache, 虚拟主机,xampp]
---
不知道说什么直接贴配置文件

httpd-vhosts.conf

	#
	# Virtual Hosts
	#
	# If you want to maintain multiple domains/hostnames on your
	# machine you can setup VirtualHost containers for them. Most configurations
	# use only name-based virtual hosts so the server doesn't need to worry about
	# IP addresses. This is indicated by the asterisks in the directives below.
	#
	# Please see the documentation at 
	# <URL:http://httpd.apache.org/docs/2.2/vhosts/>
	# for further details before you try to setup virtual hosts.
	#
	# You may use the command line option '-S' to verify your virtual host
	# configuration.

	#
	# Use name-based virtual hosting.
	#
	##NameVirtualHost *:80

	#
	# VirtualHost example:
	# Almost any Apache directive may go into a VirtualHost container.
	# The first VirtualHost section is used for all requests that do not
	# match a ServerName or ServerAlias in any <VirtualHost> block.
	#
	##<VirtualHost *:80>
	    ##ServerAdmin postmaster@dummy-host.localhost
	    ##DocumentRoot "/xampp/htdocs/dummy-host.localhost"
	    ##ServerName dummy-host.localhost
	    ##ServerAlias www.dummy-host.localhost
	    ##ErrorLog "logs/dummy-host.localhost-error.log"
	    ##CustomLog "logs/dummy-host.localhost-access.log" combined
	##</VirtualHost>

	<VirtualHost beiwang.w3nson.com:80>
	    ServerAdmin beiwang.w3nson.com
	    DocumentRoot "E:\workspace\beiwang"
	    ServerName dummy-host2.localhost
	    ##ServerAlias www.dummy-host2.localhost
	    ErrorLog "logs/dummy-host2.localhost-error.log"
	    CustomLog "logs/dummy-host2.localhost-access.log" combined
	</VirtualHost>

	<VirtualHost test.w3nson.com:80>
	    ServerAdmin test.w3nson.com
	    DocumentRoot "/xampp/htdocs"
	    ServerName dummy-host2.localhost
	    ##ServerAlias www.dummy-host2.localhost
	    ErrorLog "logs/dummy-host2.localhost-error.log"
	    CustomLog "logs/dummy-host2.localhost-access.log" combined


	</VirtualHost>

问题：需要修改 httpd.conf吗？  
答复：按照xampp的默认配置的话是不需要的。
