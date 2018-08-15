---
UID: NS:winldap.ldap
title: ldap
author: windows-sdk-content
description: Represents an LDAP session.
old-location: ldap\ldap.htm
old-project: ldap
ms.assetid: 844093e1-daba-494d-91b3-67455ff2e456
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PLDAP, LDAP, LDAP structure [LDAP], PLDAP, PLDAP structure pointer [LDAP], _ldap_ldap, ldap, ldap.ldap, winldap/LDAP, winldap/PLDAP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winldap.h
req.include-header: 
req.redist: 
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
req.typenames: LDAP, *PLDAP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap structure


## -description


The <b>LDAP</b> structure represents an LDAP session. Typically, a session corresponds to a connection to a single server. However, in the case of referrals, an LDAP session may encompass several server connections. The ability to track referrals is available in LDAP 3.


## -struct-fields


## -remarks



An <b>LDAP</b> structure is an opaque data type allocated and initialized by a call to 
<a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a>, 
<a href="https://msdn.microsoft.com/9dc62bb8-8569-4682-bfc7-7721af287318">cldap_open</a>, or 
<a href="https://msdn.microsoft.com/ebd7303d-e98d-454d-9964-d774d5c2a756">ldap_open</a>. Subsequent LDAP calls pass a handle to this structure, which maintains the state of an LDAP session for the duration of the connection. When the session ends, call 
<a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a> to destroy the connection handle.

Although this is an opaque data type, it is documented in Winldap.h. This is primarily of value in porting applications written using other LDAP client implementations. Call 
    <a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a> or 
<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a> to access or change the values associated with the LDAP connection handle (this structure). Using these two functions also expose settings not directly accessible from the <b>LDAP</b> structure. For more information about session options, see <a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>.




## -see-also




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>



<a href="https://msdn.microsoft.com/9dc62bb8-8569-4682-bfc7-7721af287318">cldap_open</a>



<a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a>



<a href="https://msdn.microsoft.com/c0aa5a9e-ed46-42fb-9c02-728afea51505">ldap_init</a>



<a href="https://msdn.microsoft.com/ebd7303d-e98d-454d-9964-d774d5c2a756">ldap_open</a>



<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>



<a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind</a>
 

 

