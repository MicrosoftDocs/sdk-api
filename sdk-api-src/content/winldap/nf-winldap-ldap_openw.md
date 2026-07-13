---
UID: NF:winldap.ldap_openW
title: ldap_openW function (winldap.h)
description: The ldap_openW (Unicode) function creates and initializes a connection block, then opens the connection to an LDAP server. It is not recommended, use the ldap_initW (Unicode) function instead.
helpviewer_keywords: ["_ldap_ldap_open", "ldap.ldap__open", "ldap.ldap_open", "ldap_open", "ldap_open function [LDAP]", "ldap_openW", "winldap/ldap_open", "winldap/ldap_openW"]
old-location: ldap\ldap_open.htm
tech.root: ldap
ms.assetid: ebd7303d-e98d-454d-9964-d774d5c2a756
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_open, ldap.ldap__open, ldap.ldap_open, ldap_open, ldap_open function [LDAP], ldap_openA, ldap_openW, winldap/ldap_open, winldap/ldap_openA, winldap/ldap_openW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_openW (Unicode) and ldap_openA (ANSI)
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
 - ldap_openW
 - winldap/ldap_openW
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
 - ldap_open
 - ldap_openA
 - ldap_openW
---

# ldap_openW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-cldap_open">ldap_open</a> is available for use in the operating systems specified in the Requirements section; however, it is not recommended. Instead, use <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a>.]

The <b>ldap_open</b> function creates and initializes a connection block, then opens the connection to an LDAP server.

## -parameters

### -param HostName [in]

A pointer to a null-terminated string. A domain name, a list of host names, or dotted strings that represent the IP address of LDAP server hosts. Use a single space to separate the host names in the list. Each host name in the list may be followed by a port number. The optional port number is separated from the host itself with a colon (:). The LDAP run time attempts connection with the hosts in the order listed, stopping when a successful connection is made. Be aware that only <b>ldap_open</b> attempts to make the connection before returning to the caller. The function 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a> does not connect to the LDAP server.

### -param PortNumber [in]

Contains the TCP port number to which to connect. The default LDAP port, 389, can be obtained by supplying the constant <b>LDAP_PORT</b>. If a host name includes a port number then this parameter is ignored.

## -returns

If the function succeeds, it returns a session handle, in the form of a pointer to an LDAP data structure. Free the session handle, when no longer required,  with a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>.

If the function fails, it returns <b>NULL</b>. Use the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> function to retrieve the error code.

## -remarks

Call <b>ldap_open</b> to create a connection block to an LDAP server. The  <i>HostName</i> can be <b>NULL</b> in which case the run time attempts to find the default LDAP server. The host names are tried in the order listed, stopping with the first successful connection. For Active Directory servers, the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function can be used to obtain name of the server, which can then be passed as the <i>HostName</i> parameter instead of using <b>NULL</b>.

If the <i>HostName</i> was set to either <b>NULL</b> or the domain name, automatic reconnect applies. If the connected DC stops functioning for some reason during the connection's lifetime, LDAP will automatically reconnect to another DC in the specified domain. This behavior can be toggled off or on using the <b>LDAP_OPT_AUTO_RECONNECT</b> session option, which is on by default.

The default LDAP server is a Microsoft specific option when you use <b>LDAP_OPT_HOST_NAME</b>. This option specifies the host name of the default LDAP server and returns the host name of the server in Unicode or ANSI, contingent on the use of <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_optionW</a> or <b>ldap_get_optionA</b>, respectively.

If a Global Catalog port number is passed to <b>ldap_open</b> as one of the arguments, then the <i>HostName</i> passed for that port number must be the name of the forest for the underlying call to <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName()</a> to correctly find the GC in the enterprise.

The <b>ldap_open</b> function allocates an LDAP data structure to maintain state data for the session and returns a handle to this structure. Pass this handle to subsequent LDAP function calls during the course of the session.

Multithreading: Calls to <b>ldap_open</b> are thread-safe.

<div class="alert"><b>Note</b>  <b>ldap_open</b> is heavily deprecated by the current LDAP RFC because it immediately opens a session to the domain controller without giving the calling application a chance to configure any session options, for example (and most importantly) security-related session options. Users are encouraged to use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a> as the preferred method of initializing an LDAP session.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_open as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-cldap_open">cldap_open</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
