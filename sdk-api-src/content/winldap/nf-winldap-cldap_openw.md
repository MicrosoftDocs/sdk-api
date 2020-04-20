---
UID: NF:winldap.cldap_openW
title: cldap_openW function (winldap.h)
description: Establishes a session with an LDAP server over a connectionless User Datagram Protocol (UDP) service.helpviewer_keywords: ["_ldap_cldap_open","cldap_open","cldap_open function [LDAP]","cldap_openA","cldap_openW","ldap.cldap__open","ldap.cldap_open","winldap/cldap_open","winldap/cldap_openA","winldap/cldap_openW"]
old-location: ldap\cldap_open.htm
tech.root: ldap
ms.assetid: 9dc62bb8-8569-4682-bfc7-7721af287318
ms.date: 12/05/2018
ms.keywords: _ldap_cldap_open, cldap_open, cldap_open function [LDAP], cldap_openA, cldap_openW, ldap.cldap__open, ldap.cldap_open, winldap/cldap_open, winldap/cldap_openA, winldap/cldap_openW
f1_keywords:
- winldap/cldap_open
dev_langs:
- c++
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: cldap_openW (Unicode) and cldap_openA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wldap32.dll
api_name:
- cldap_open
- cldap_openA
- cldap_openW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# cldap_openW function


## -description


The <b>cldap_open</b> function establishes a session with an LDAP server over a connectionless User Datagram Protocol (UDP) service. This is an alternate to using TCP/IP.


## -parameters




### -param HostName [in]

A pointer to a null-terminated string that contains a list of host names or dotted strings that represent the IP address of LDAP server hosts. Use a single space to separate the host names in the list. Each host name in the list may be followed by a port number. The optional port number is separated from the host itself with a colon (:). The LDAP run time attempts connection with the hosts in the order listed, stopping when a successful connection is made.


### -param PortNumber [in]

The port number to be used. If no port number is specified, the default is port 389, which is defined as LDAP_PORT. If  port numbers are included in the <i>HostName</i> parameter, this parameter is ignored.


## -returns



If the function succeeds, a session handle, in the form of a pointer to an LDAP structure is returned. Free the session handle with a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> when it is no longer required.

If the function fails, the return value is <b>NULL</b>. To get the error code, call 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> or the Win32 function 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>cldap_open</b> function, unlike 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>, creates a connection block for UDP-based connectionless LDAP services. No TCP session is maintained. Like <b>ldap_open</b>, <b>cldap_open</b> allocates an LDAP structure to maintain state data for the session, and then attempts to make the connection before returning to the caller. The call returns a session handle, which you pass to subsequent LDAP function calls in the course of the session. When finished with the session, always free the allocated session handle by using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>.

Using LDAP over UDP does not support binding and does not support TLS (SSL) or SASL.

Multithreading: Calls to <b>cldap_open</b> are thread-safe.

<div class="alert"><b>Note</b>  When using <b>cldap_open</b>, the connection is opened by an anonymous user.  The only available operations are those that an anonymous user can run.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
 

 

