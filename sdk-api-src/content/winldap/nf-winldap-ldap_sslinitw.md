---
UID: NF:winldap.ldap_sslinitW
title: ldap_sslinitW function (winldap.h)
description: The ldap_sslinitW (Unicode) function (winldap.h) initializes a Secure Sockets Layer (SSL) session with an LDAP server.
helpviewer_keywords: ["_ldap_ldap_sslinit", "ldap.ldap__sslinit", "ldap.ldap_sslinit", "ldap_sslinit", "ldap_sslinit function [LDAP]", "ldap_sslinitW", "winldap/ldap_sslinit", "winldap/ldap_sslinitW"]
old-location: ldap\ldap_sslinit.htm
tech.root: ldap
ms.assetid: 04c13577-9d9f-4305-8aa2-fad81c03290a
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_sslinit, ldap.ldap__sslinit, ldap.ldap_sslinit, ldap_sslinit, ldap_sslinit function [LDAP], ldap_sslinitA, ldap_sslinitW, winldap/ldap_sslinit, winldap/ldap_sslinitA, winldap/ldap_sslinitW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_sslinitW (Unicode) and ldap_sslinitA (ANSI)
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
 - ldap_sslinitW
 - winldap/ldap_sslinitW
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
 - ldap_sslinit
 - ldap_sslinitA
 - ldap_sslinitW
---

# ldap_sslinitW function


## -description

The <b>ldap_sslinit</b> function initializes a Secure Sockets Layer (SSL) session with an LDAP server.

## -parameters

### -param HostName [in]

A pointer to a null-terminated string that contains a space-separated list of host names or dotted strings representing the IP address of hosts running an LDAP server to which to connect. Each host name in the list can include an optional port number which is separated from the host itself with a colon (:) character.

### -param PortNumber [in]

Contains the TCP port number to which to connect. Set to <b>LDAP_SSL_PORT</b> to obtain the default port, 636. This parameter is ignored if a host name includes a port number.

### -param secure [in]

If nonzero, the function uses SSL encryption. If the value is 0, the function establishes a plain TCP connection and uses clear text (no encryption).

## -returns

If the function succeeds, it returns a session handle, in the form of a pointer to an 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> structure. The session handle must be freed with a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> when it is no longer needed.

If the function fails, the return value is <b>NULL</b>. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> to retrieve the error code.

## -remarks

Call <b>ldap_sslinit</b> to create a connection block to a secured LDAP server. The <i>HostName</i> parameter can be <b>NULL</b> in which case the run time attempts to find the "default" LDAP server. The hosts are tried in the order listed, stopping with the first one to which a successful connection is made.

If the <i>HostName</i> was set to either <b>NULL</b> or the domain name, automatic reconnect applies. If the connected DC stops functioning for some reason during the connection's lifetime, LDAP will automatically reconnect to another DC in the specified domain. This behavior can be toggled off or on using the <b>LDAP_OPT_AUTO_RECONNECT</b> session option, which is on by default.

If a Global Catalog port number is passed to <b>ldap_sslinit</b> as one of the arguments, then the <i>HostName</i> passed for that port number must be the name of the forest for the underlying call to <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> to correctly find the GC in the enterprise.

The function allocates an LDAP structure to maintain state information for the session, and returns a handle to this structure. You pass this handle to subsequent LDAP function calls during the course of the session.

Multithreading: Calls to <b>ldap_sslinit</b> are thread-safe.

Microsoft implements security features, like SSL, through its SSPI capabilities.





> [!NOTE]
> The winldap.h header defines ldap_sslinit as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/initializing-a-session">Initializing a Session</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>



<a href="/windows/desktop/SecAuthN/sspi-options-for-distributed-applications">SSPI Options for Distributed Applications</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
