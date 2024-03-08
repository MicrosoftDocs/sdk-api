---
UID: NF:azroles.IAzApplicationGroup.AddPropertyItem
title: IAzApplicationGroup::AddPropertyItem (azroles.h)
description: Adds the specified entity to the specified list. (IAzApplicationGroup.AddPropertyItem)
helpviewer_keywords: ["AZ_PROP_GROUP_APP_MEMBERS","AZ_PROP_GROUP_APP_NON_MEMBERS","AZ_PROP_GROUP_MEMBERS","AZ_PROP_GROUP_MEMBERS_NAME","AZ_PROP_GROUP_NON_MEMBERS","AZ_PROP_GROUP_NON_MEMBERS_NAME","AddPropertyItem","AddPropertyItem method [Security]","AddPropertyItem method [Security]","AzApplicationGroup object","AddPropertyItem method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddPropertyItem method","IAzApplicationGroup interface [Security]","AddPropertyItem method","IAzApplicationGroup.AddPropertyItem","IAzApplicationGroup::AddPropertyItem","azroles/IAzApplicationGroup::AddPropertyItem","security.iazapplicationgroup_addpropertyitem"]
old-location: security\iazapplicationgroup_addpropertyitem.htm
tech.root: security
ms.assetid: 7a7a11ad-42f9-4d3f-8d55-6e8b3e1bea7e
ms.date: 03/20/2023
ms.keywords: AZ_PROP_GROUP_APP_MEMBERS, AZ_PROP_GROUP_APP_NON_MEMBERS, AZ_PROP_GROUP_MEMBERS, AZ_PROP_GROUP_MEMBERS_NAME, AZ_PROP_GROUP_NON_MEMBERS, AZ_PROP_GROUP_NON_MEMBERS_NAME, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzApplicationGroup object, AddPropertyItem method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddPropertyItem method, IAzApplicationGroup interface [Security],AddPropertyItem method, IAzApplicationGroup.AddPropertyItem, IAzApplicationGroup::AddPropertyItem, azroles/IAzApplicationGroup::AddPropertyItem, security.iazapplicationgroup_addpropertyitem
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
 - IAzApplicationGroup::AddPropertyItem
 - azroles/IAzApplicationGroup::AddPropertyItem
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
 - IAzApplicationGroup.AddPropertyItem
 - AzApplicationGroup.AddPropertyItem
---

# IAzApplicationGroup::AddPropertyItem

## -description

The **AddPropertyItem** method adds the specified entity to the specified list.

## -parameters

### -param lPropId [in]

Property ID of the list to which to add the entity specified by the _varProp_ parameter.

The following table shows the possible values:

| Value | Meaning |
|--------|--------|
| `AZ_PROP_GROUP_APP_MEMBERS` | Can also be added using the [AddAppMember](nf-azroles-iazapplicationgroup-addappmember.md) method. |
| `AZ_PROP_GROUP_APP_NON_MEMBERS` | Can also be added using the [AddAppNonMember](nf-azroles-iazapplicationgroup-addappnonmember.md) method. |
| `AZ_PROP_GROUP_MEMBERS` | Can also be added using the [AddMember](nf-azroles-iazapplicationgroup-addmember.md) method. |
| `AZ_PROP_GROUP_MEMBERS_NAME` | Can also be added using the [AddMemberName](nf-azroles-iazapplicationgroup-addmembername.md) method. |
| `AZ_PROP_GROUP_NON_MEMBERS` | Can also be added using the [AddNonMember](nf-azroles-iazapplicationgroup-addnonmember.md) method. |
| `AZ_PROP_GROUP_NON_MEMBERS_NAME` | Can also be added using the [AddNonMemberName](nf-azroles-iazapplicationgroup-addnonmembername.md) method. |

### -param varProp

TBD

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

You must call the [Submit](nf-azroles-iazapplicationgroup-submit.md) method to persist any changes made by this method.

## -see-also

[AddMember](nf-azroles-iazapplicationgroup-addmember.md)

[Submit](nf-azroles-iazapplicationgroup-submit.md)
