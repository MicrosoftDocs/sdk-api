---
UID: NF:azroles.IAzApplicationGroup.put_LdapQuery
title: IAzApplicationGroup::put_LdapQuery (azroles.h)
description: Sets or retrieves the Lightweight Directory Access Protocol (LDAP) query used to define membership for an LDAP query application group. (Put)
helpviewer_keywords: ["AzApplicationGroup object [Security]","LdapQuery property","IAzApplicationGroup interface [Security]","LdapQuery property","IAzApplicationGroup.LdapQuery","IAzApplicationGroup.put_LdapQuery","IAzApplicationGroup::LdapQuery","IAzApplicationGroup::get_LdapQuery","IAzApplicationGroup::put_LdapQuery","LdapQuery property [Security]","LdapQuery property [Security]","AzApplicationGroup object","LdapQuery property [Security]","IAzApplicationGroup interface","azroles/IAzApplicationGroup::LdapQuery","azroles/IAzApplicationGroup::get_LdapQuery","azroles/IAzApplicationGroup::put_LdapQuery","put_LdapQuery","security.iazapplicationgroup_ldapquery"]
old-location: security\iazapplicationgroup_ldapquery.htm
tech.root: security
ms.assetid: 963ee516-6dd5-419f-9186-578b7fe9c5bc
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],LdapQuery property, IAzApplicationGroup interface [Security],LdapQuery property, IAzApplicationGroup.LdapQuery, IAzApplicationGroup.put_LdapQuery, IAzApplicationGroup::LdapQuery, IAzApplicationGroup::get_LdapQuery, IAzApplicationGroup::put_LdapQuery, LdapQuery property [Security], LdapQuery property [Security],AzApplicationGroup object, LdapQuery property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::LdapQuery, azroles/IAzApplicationGroup::get_LdapQuery, azroles/IAzApplicationGroup::put_LdapQuery, put_LdapQuery, security.iazapplicationgroup_ldapquery
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplicationGroup::put_LdapQuery
 - azroles/IAzApplicationGroup::put_LdapQuery
dev_langs:
 - c++
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
---

# IAzApplicationGroup::put_LdapQuery


## -description

The <b>LdapQuery</b> property sets or retrieves the <a href="/windows/desktop/SecGloss/l-gly">Lightweight Directory Access Protocol</a> (LDAP) query used to define membership for an LDAP query application group.

This property is read/write.

## -parameters

## -remarks

This property is ignored unless the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_type">Type</a> property is AZ_GROUPTYPE_LDAP_QUERY. 

The maximum length of this property is 4,096 characters.
