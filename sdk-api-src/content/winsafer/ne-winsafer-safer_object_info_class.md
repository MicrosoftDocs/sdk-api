---
UID: NE:winsafer._SAFER_OBJECT_INFO_CLASS
title: SAFER_OBJECT_INFO_CLASS (winsafer.h)
description: Defines the type of information requested about a Safer object.
helpviewer_keywords: ["SAFER_OBJECT_INFO_CLASS","SAFER_OBJECT_INFO_CLASS enumeration [Security]","SaferObjectAllIdentificationGuids","SaferObjectDescription","SaferObjectExtendedError","SaferObjectFriendlyName","SaferObjectLevelId","SaferObjectScopeId","SaferObjectSingleIdentification","security.safer_object_info_class","winsafer/SAFER_OBJECT_INFO_CLASS","winsafer/SaferObjectAllIdentificationGuids","winsafer/SaferObjectDescription","winsafer/SaferObjectExtendedError","winsafer/SaferObjectFriendlyName","winsafer/SaferObjectLevelId","winsafer/SaferObjectScopeId","winsafer/SaferObjectSingleIdentification"]
old-location: security\safer_object_info_class.htm
tech.root: security
ms.assetid: 31de9e42-6795-433a-937f-c4243e4961df
ms.date: 12/05/2018
ms.keywords: SAFER_OBJECT_INFO_CLASS, SAFER_OBJECT_INFO_CLASS enumeration [Security], SaferObjectAllIdentificationGuids, SaferObjectDescription, SaferObjectExtendedError, SaferObjectFriendlyName, SaferObjectLevelId, SaferObjectScopeId, SaferObjectSingleIdentification, security.safer_object_info_class, winsafer/SAFER_OBJECT_INFO_CLASS, winsafer/SaferObjectAllIdentificationGuids, winsafer/SaferObjectDescription, winsafer/SaferObjectExtendedError, winsafer/SaferObjectFriendlyName, winsafer/SaferObjectLevelId, winsafer/SaferObjectScopeId, winsafer/SaferObjectSingleIdentification
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SAFER_OBJECT_INFO_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAFER_OBJECT_INFO_CLASS
 - winsafer/_SAFER_OBJECT_INFO_CLASS
 - SAFER_OBJECT_INFO_CLASS
 - winsafer/SAFER_OBJECT_INFO_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_OBJECT_INFO_CLASS
---

# SAFER_OBJECT_INFO_CLASS enumeration


## -description

The <b>SAFER_OBJECT_INFO_CLASS</b> enumeration type defines the type of information requested about a Safer object.

## -enum-fields

### -field SaferObjectLevelId:1

Queries for the LEVELID constant.

### -field SaferObjectScopeId

Queries for the user or machine scope.

### -field SaferObjectFriendlyName

Queries for the display name.

### -field SaferObjectDescription

Queries for the description.

### -field SaferObjectBuiltin

### -field SaferObjectDisallowed

### -field SaferObjectDisableMaxPrivilege

### -field SaferObjectInvertDeletedPrivileges

### -field SaferObjectDeletedPrivileges

### -field SaferObjectDefaultOwner

### -field SaferObjectSidsToDisable

### -field SaferObjectRestrictedSidsInverted

### -field SaferObjectRestrictedSidsAdded

### -field SaferObjectAllIdentificationGuids

Queries for all levels.

### -field SaferObjectSingleIdentification

Queries for a single additional rule.

### -field SaferObjectExtendedError

Queries for additional error codes set during rule processing.

## -remarks

The <b>SAFER_OBJECT_INFO_CLASS</b> enumeration type is used by the <a href="/windows/desktop/api/winsafer/nf-winsafer-safergetlevelinformation">SaferGetLevelInformation</a> function.
