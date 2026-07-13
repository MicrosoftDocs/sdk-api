---
UID: NF:winldap.ldap_initW
title: ldap_initW function (winldap.h)
description: The ldap_initW (Unicode) function (winldap.h) initializes a session with an LDAP server. 
helpviewer_keywords: ["_ldap_ldap_init", "ldap.ldap__init", "ldap.ldap_init", "ldap_init", "ldap_init function [LDAP]", "ldap_initW", "winldap/ldap_init", "winldap/ldap_initW"]
old-location: ldap\ldap_init.htm
tech.root: ldap
ms.assetid: c0aa5a9e-ed46-42fb-9c02-728afea51505
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_init, ldap.ldap__init, ldap.ldap_init, ldap_init, ldap_init function [LDAP], ldap_initA, ldap_initW, winldap/ldap_init, winldap/ldap_initA, winldap/ldap_initW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_initW (Unicode) and ldap_initA (ANSI)
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
 - ldap_initW
 - winldap/ldap_initW
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
 - ldap_init
 - ldap_initA
 - ldap_initW
---

# ldap_initW function


## -description

The <b>ldap_init</b> function initializes a session with an LDAP server.

## -parameters

### -param HostName [in]

A pointer to a null-terminated string that contains a domain name, or a space-separated list of host names or dotted strings that represent the IP address of hosts running an LDAP server to which to connect. Each host name in the list can include an optional port number which is separated from the host itself with a colon (:). For more information about the use of the <b>LDAP_OPT_AREC_EXCLUSIVE</b> option when connecting to Active Directory servers, see the Remarks section.

### -param PortNumber [in]

Contains the TCP port number to which to connect. Set to <b>LDAP_PORT</b> to obtain the default port, 389. This parameter is ignored if a host name includes a port number.

## -returns

If the function succeeds, it returns a session handle, in the form of a pointer to an 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> data structure. The session handle must be freed with a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> when it is no longer required.

If the function fails, it returns <b>NULL</b>. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> to retrieve the error code.

## -remarks

Call <b>ldap_init</b> to create a connection block to an LDAP server. Unlike 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>, a call to <b>ldap_init</b> does not open the connection. You can call <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_connect">ldap_connect</a> explicitly to have the library contact the server. This is useful when you want to specify a local timeout in which case you would call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>, with the connection block from <b>ldap_init</b>, before calling <b>ldap_connect</b>. Typically, however, this call is unnecessary because the first operation function that requires an open connection calls <b>ldap_connect</b> internally if it has not  been called.

The function allocates an LDAP data structure to maintain state data for the session, and returns a handle to this structure. Pass this handle to LDAP function calls during the session.

The <i>HostName</i> parameter can be <b>NULL</b>, in which case the run time attempts to find the "default" LDAP server. When 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_connect">ldap_connect</a> is called, the hosts are attempted in the order listed, stopping with the first successful connection. For Active Directory servers, the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function can be used to obtain name of the server, which can then be passed as the <i>HostName</i> parameter instead of using <b>NULL</b>.

Even when the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a> function  is used to set the <b>LDAP_OPT_GETDSNAME_FLAGS</b> option, which in turn specifies the flags that will be passed to <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDCName</a> to discover which DC to connect to. The LDAP client also passes the  <b>DS_ONLY_LDAP_NEEDED</b> flag to <b>DsGetDCName</b> in addition to the flags that <b>LDAP_OPT_GETDSNAME_FLAGS</b> specifies.

If <b>NULL</b> is passed for the <i>HostName</i> parameter and the calling computer is a member of an Active Directory domain, then the runtime will search for a DC in the domain in which the current computer is a member when attempting to connect.

If <b>NULL</b> is passed for the <i>HostName</i> parameter and the calling computer is a DC of an Active Directory domain, then the runtime will switch <b>NULL</b> with 127.0.0.1 and connect to the local computer using loopback when attempting to connect.

If an Active Directory domain name is passed for the <i>HostName</i> parameter, then <b>ldap_init</b> will find the "default" LDAP server in that domain.

If the <i>HostName</i> was set to either <b>NULL</b> or the domain name, automatic reconnect applies. If the connected DC stops functioning for some reason during the connection's lifetime, LDAP will automatically reconnect to another DC in the specified domain. This behavior can be toggled off or on using the <b>LDAP_OPT_AUTO_RECONNECT</b> session option, which is on by default.

If an Active Directory DNS server name is passed for the <i>HostName</i> parameter, then 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a> should be called to set the <b>LDAP_OPT_AREC_EXCLUSIVE</b> flag on before calling any LDAP function that creates the actual connection.  This forces an A-record lookup and bypasses any SRV record lookup when resolving the host name.  In the case of a branch office with a dial-up connection, using A-Record lookup can avoid forcing the dialup to query a remote DNS server for SRV records when resolving names.

If a Global Catalog port number is passed to <b>ldap_init</b> as one of the arguments, then the <i>HostName</i> passed for that port number must be the name of the forest for the underlying call to <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName()</a> to correctly find the GC in the enterprise.

Multithreading: A call to <b>ldap_init</b> is thread safe.

<div class="alert"><b>Note</b>  <b>ldap_init</b> is the preferred method of initializing an LDAP session. The use of <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a> is heavily deprecated by the current LDAP RFC because it precludes the use of setting any session options.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_init as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/initializing-a-session">Initializing a Session</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_connect">ldap_connect</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_open">ldap_open</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>
