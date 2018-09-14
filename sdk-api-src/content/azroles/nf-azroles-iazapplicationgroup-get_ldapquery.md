---
UID: NF:azroles.IAzApplicationGroup.get_LdapQuery
title: IAzApplicationGroup::get_LdapQuery
author: windows-sdk-content
description: Sets or retrieves the Lightweight Directory Access Protocol (LDAP) query used to define membership for an LDAP query application group.
old-location: security\iazapplicationgroup_ldapquery.htm
tech.root: secauthz
ms.assetid: 963ee516-6dd5-419f-9186-578b7fe9c5bc
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AzApplicationGroup object [Security],LdapQuery property, IAzApplicationGroup interface [Security],LdapQuery property, IAzApplicationGroup.LdapQuery, IAzApplicationGroup.get_LdapQuery, IAzApplicationGroup::LdapQuery, IAzApplicationGroup::get_LdapQuery, IAzApplicationGroup::put_LdapQuery, LdapQuery property [Security], LdapQuery property [Security],AzApplicationGroup object, LdapQuery property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::LdapQuery, azroles/IAzApplicationGroup::get_LdapQuery, azroles/IAzApplicationGroup::put_LdapQuery, get_LdapQuery, security.iazapplicationgroup_ldapquery
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplicationGroup.LdapQuery
 - IAzApplicationGroup.get_LdapQuery
 - IAzApplicationGroup.put_LdapQuery
 - AzApplicationGroup.LdapQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplicationGroup::get_LdapQuery


## -description


The <b>LdapQuery</b> property sets or retrieves the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Lightweight Directory Access Protocol</a> (LDAP) query used to define membership for an LDAP query application group.

This property is read/write.


## -parameters


## -remarks



This property is ignored unless the <a href="https://msdn.microsoft.com/dc100895-4cfb-4e02-97bc-5c99bf26fbe2">Type</a> property is AZ_GROUPTYPE_LDAP_QUERY. 

The maximum length of this property is 4,096 characters.



