---
UID: NS:winldap.ldapmsg
title: LDAPMessage (winldap.h)
description: Used by an LDAP function to return results and error data.
helpviewer_keywords: ["*PLDAPMessage","LDAPMessage","LDAPMessage structure [LDAP]","PLDAPMessage","PLDAPMessage structure pointer [LDAP]","_ldap_ldapmessage","ldap.ldapmessage","winldap/LDAPMessage","winldap/PLDAPMessage"]
old-location: ldap\ldapmessage.htm
tech.root: ldap
ms.assetid: 547a0736-23a4-4bfd-8ae0-866825228b53
ms.date: 12/05/2018
ms.keywords: '*PLDAPMessage, LDAPMessage, LDAPMessage structure [LDAP], PLDAPMessage, PLDAPMessage structure pointer [LDAP], _ldap_ldapmessage, ldap.ldapmessage, winldap/LDAPMessage, winldap/PLDAPMessage'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LDAPMessage, *PLDAPMessage
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldapmsg
 - winldap/ldapmsg
 - PLDAPMessage
 - winldap/PLDAPMessage
 - LDAPMessage
 - winldap/LDAPMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAPMessage
---

# LDAPMessage structure


## -description

The <b>LDAPMessage</b> structure is used by an LDAP function to return results and error data.

## -struct-fields

## -remarks

The <b>LDAPMessage</b> structure is an opaque data type returned from a server when you call a search or a traversal function. For example, after performing an asynchronous operation,  <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> can be called to get the server <b>LDAPMessage</b> response. Another example is  a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_s">ldap_search_s</a>, which also returns an <b>LDAPMessage</b>.

To free the <b>LDAPMessage</b> structure when it is no longer required, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>.

There are no client-accessible fields in this structure.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>



<a href="/previous-versions/windows/desktop/ldap/functions">functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_entries">ldap_count_entries</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search">ldap_search</a>