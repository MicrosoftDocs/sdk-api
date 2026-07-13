---
UID: NF:winldap.cldap_openW
title: cldap_openW function (winldap.h)
description: The cldap_openW (Unicode) function (winldap.h) establishes a session with an LDAP server over a connectionless User Datagram Protocol (UDP) service. 
helpviewer_keywords: ["_ldap_cldap_open", "cldap_open", "cldap_open function [LDAP]", "cldap_openW", "ldap.cldap__open", "ldap.cldap_open", "winldap/cldap_open", "winldap/cldap_openW"]
old-location: ldap\cldap_open.htm
tech.root: ldap
ms.assetid: 9dc62bb8-8569-4682-bfc7-7721af287318
ms.date: 08/08/2022
ms.keywords: _ldap_cldap_open, cldap_open, cldap_open function [LDAP], cldap_openA, cldap_openW, ldap.cldap__open, ldap.cldap_open, winldap/cldap_open, winldap/cldap_openA, winldap/cldap_openW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - cldap_openW
 - winldap/cldap_openW
dev_langs:
 - c++
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

If the function succeeds, a session handle, in the form of a pointer to an LDAP structure is returned. Free the session handle with a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> when it is no longer required.

If the function fails, the return value is <b>NULL</b>. To get the error code, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> or the Win32 function 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>cldap_open</b> function, unlike 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>, creates a connection block for UDP-based connectionless LDAP services. No TCP session is maintained. Like <b>ldap_open</b>, <b>cldap_open</b> allocates an LDAP structure to maintain state data for the session, and then attempts to make the connection before returning to the caller. The call returns a session handle, which you pass to subsequent LDAP function calls in the course of the session. When finished with the session, always free the allocated session handle by using <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>.

Using LDAP over UDP does not support binding and does not support TLS (SSL) or SASL.

Multithreading: Calls to <b>cldap_open</b> are thread-safe.

<div class="alert"><b>Note</b>  When using <b>cldap_open</b>, the connection is opened by an anonymous user.  The only available operations are those that an anonymous user can run.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines cldap_open as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
