---
UID: NF:winldap.ldap_conn_from_msg
title: ldap_conn_from_msg function (winldap.h)
description: Returns the LDAP session handle (connection pointer) for a particular message.
helpviewer_keywords: ["_ldap_ldap_conn_from_msg","ldap.ldap__conn__from__msg","ldap.ldap_conn_from_msg","ldap_conn_from_msg","ldap_conn_from_msg function [LDAP]","winldap/ldap_conn_from_msg"]
old-location: ldap\ldap_conn_from_msg.htm
tech.root: ldap
ms.assetid: 0f536c42-06c1-43d9-a298-4a9e9bf96a46
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_conn_from_msg, ldap.ldap__conn__from__msg, ldap.ldap_conn_from_msg, ldap_conn_from_msg, ldap_conn_from_msg function [LDAP], winldap/ldap_conn_from_msg
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
 - ldap_conn_from_msg
 - winldap/ldap_conn_from_msg
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
 - ldap_conn_from_msg
---

# ldap_conn_from_msg function


## -description

The <b>ldap_conn_from_msg</b> function returns the <a href="/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle (connection pointer) for a particular message.

## -parameters

### -param PrimaryConn [in]

A pointer to the <a href="/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle of the message, if known. If the <b>LDAP</b> session handle for the message is unknown, then <b>NULL</b> may be passed for this parameter provided that the 
<a href="/previous-versions/windows/desktop/ldap/session-options">LDAP_OPT_REF_DEREF_CONN_PER_MSG</a> session option had been previously set for the message session.

### -param res [in]

The <b>LDAP</b> message queried.  If <b>NULL</b> is passed for this parameter, then the function will respond with a <b>NULL</b> return value.

## -returns

The return value is the <a href="/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle (connection pointer) where the message originated from. This function returns <b>NULL</b> if the originating session has closed or if a <b>NULL</b> <b>LDAPMessage</b> pointer is passed to the function and the <a href="/previous-versions/windows/desktop/ldap/session-options">LDAP_OPT_REF_DEREF_CONN_PER_MSG</a> session option was not previously set for the message session.

## -remarks

This function is used to identify the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle associated with the specified <b>LDAP</b> message. It returns a valid <b>LDAP</b> session handle only if one of the following  conditions are met:

<ul>
<li>The <a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a> originated from the same <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session handle passed to the function in the <i>PrimaryConn</i> parameter.</li>

<li>The <a href="/previous-versions/windows/desktop/ldap/session-options">LDAP_OPT_REF_DEREF_CONN_PER_MSG</a> session option was previously enabled on the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> session associated with the message.</li>
</ul>
If neither of these conditions are met, the function returns a <b>NULL</b> session handle.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/establishing-an-ldap-session">Establishing an LDAP Session</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>


<a href="/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/windows/desktop/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a>


<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>



<a href="/previous-versions/windows/desktop/ldap/data-structures">structures</a>