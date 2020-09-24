---
UID: NF:winldap.ldap_connect
title: ldap_connect function (winldap.h)
description: The ldap_connect function establishes a connection with the server.
helpviewer_keywords: ["_ldap_ldap_connect","ldap.ldap__connect","ldap.ldap_connect","ldap_connect","ldap_connect function [LDAP]","winldap/ldap_connect"]
old-location: ldap\ldap_connect.htm
tech.root: ldap
ms.assetid: 783e52fd-d758-47ba-b350-878a2efec8a3
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_connect, ldap.ldap__connect, ldap.ldap_connect, ldap_connect, ldap_connect function [LDAP], winldap/ldap_connect
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ldap_connect
 - winldap/ldap_connect
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
 - ldap_connect
---

# ldap_connect function


## -description

The <b>ldap_connect</b> function establishes a connection with the server.

## -parameters

### -param ld [in]

The session handle obtained from <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a>.

### -param timeout [in]

A pointer to an <a href="/windows/win32/api/winldap/ns-winldap-ldap_timeval">LDAP_TIMEVAL</a> structure that specifies the number of seconds to spend in an attempt to establish a connection before a timeout. If <b>NULL</b>, the function uses a default timeout value.

## -returns

If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see <a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Although it is not required that a client call <b>ldap_connect</b> to establish a connection to the server, it is good programming practice to do so. If the connection does not exist, other functions, for example,  <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind_s">ldap_bind_s</a>, perform the call internally. However, if you have to troubleshoot this part of your application, establishing the connection prior to making the call to some other function, for example <b>ldap_bind_s</b>, will also separate the possible problems if the connection fails. Alternately,  you can specify additional options on the connection block. For example, a client can call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a> to initialize a session, then call 
<b>ldap_connect</b>, with a non-<b>NULL</b> timeout parameter value, to connect to the server with a specified time-out.

If the call to <b>ldap_connect</b> succeeds, the client is connected to the LDAP server as an  anonymous user. The session handle should be freed with a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> when it is no longer required.

If the <b>ldap_connect</b> call fails, the session handle should be freed with a call to  <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a> when no longer required for error recovery.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/establishing-an-ldap-session">Establishing an LDAP Session</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>


<a href="/windows/win32/api/winldap/ns-winldap-ldap_timeval">LDAP_TIMEVAL</a>


<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind</a>