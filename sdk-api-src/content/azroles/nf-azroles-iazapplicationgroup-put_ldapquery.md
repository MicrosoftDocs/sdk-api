---
UID: NF:azroles.IAzApplicationGroup.put_LdapQuery
title: IAzApplicationGroup::put_LdapQuery
author: windows-sdk-content
description: Sets or retrieves the Lightweight Directory Access Protocol (LDAP) query used to define membership for an LDAP query application group.
old-location: security\iazapplicationgroup_ldapquery.htm
old-project: SecAuthZ
ms.assetid: 963ee516-6dd5-419f-9186-578b7fe9c5bc
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzApplicationGroup object [Security],LdapQuery property, IAzApplicationGroup interface [Security],LdapQuery property, IAzApplicationGroup.LdapQuery, IAzApplicationGroup.put_LdapQuery, IAzApplicationGroup::LdapQuery, IAzApplicationGroup::get_LdapQuery, IAzApplicationGroup::put_LdapQuery, LdapQuery property [Security], LdapQuery property [Security],AzApplicationGroup object, LdapQuery property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::LdapQuery, azroles/IAzApplicationGroup::get_LdapQuery, azroles/IAzApplicationGroup::put_LdapQuery, put_LdapQuery, security.iazapplicationgroup_ldapquery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzApplicationGroup.LdapQuery
-	IAzApplicationGroup.get_LdapQuery
-	IAzApplicationGroup.put_LdapQuery
-	AzApplicationGroup.LdapQuery
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplicationGroup::put_LdapQuery


## -description


The <b>LdapQuery</b> property sets or retrieves the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Lightweight Directory Access Protocol</a> (LDAP) query used to define membership for an LDAP query application group.

This property is read/write.


## -parameters


## -remarks



This property is ignored unless the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property is AZ_GROUPTYPE_LDAP_QUERY. 

The maximum length of this property is 4,096 characters.



