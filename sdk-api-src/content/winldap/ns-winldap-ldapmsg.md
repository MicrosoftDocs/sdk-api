---
UID: NS:winldap.ldapmsg
title: ldapmsg
author: windows-sdk-content
description: Used by an LDAP function to return results and error data.
old-location: ldap\ldapmessage.htm
old-project: ldap
ms.assetid: 547a0736-23a4-4bfd-8ae0-866825228b53
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PLDAPMessage, LDAPMessage, LDAPMessage structure [LDAP], PLDAPMessage, PLDAPMessage structure pointer [LDAP], _ldap_ldapmessage, ldap.ldapmessage, ldapmsg, winldap/LDAPMessage, winldap/PLDAPMessage"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: LDAPMessage, *PLDAPMessage
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAPMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ldapmsg structure


## -description


The <b>LDAPMessage</b> structure is used by an LDAP function to return results and error data.


## -struct-fields


## -remarks



The <b>LDAPMessage</b> structure is an opaque data type returned from a server when you call a search or a traversal function. For example, after performing an asynchronous operation,  <a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> can be called to get the server <b>LDAPMessage</b> response. Another example is  a call to <a href="https://msdn.microsoft.com/ed0a2c43-c38f-4991-b652-a1df4f739478">ldap_search_s</a>, which also returns an <b>LDAPMessage</b>.

To free the <b>LDAPMessage</b> structure when it is no longer required, call 
<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>.

There are no client-accessible fields in this structure.




## -see-also




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">functions</a>



<a href="https://msdn.microsoft.com/6e53b914-2ad8-408a-9671-50a01a8a42f1">ldap_count_entries</a>



<a href="https://msdn.microsoft.com/a4292638-0686-4c2d-8c51-1d5d079d5782">ldap_msgfree</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/fe0d782b-8faf-4666-a952-e2bfd33f6d67">ldap_search</a>
 

 

