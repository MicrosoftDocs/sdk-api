---
UID: NE:winsafer._SAFER_OBJECT_INFO_CLASS
title: "_SAFER_OBJECT_INFO_CLASS"
author: windows-sdk-content
description: Defines the type of information requested about a Safer object.
old-location: security\safer_object_info_class.htm
old-project: SecMgmt
ms.assetid: 31de9e42-6795-433a-937f-c4243e4961df
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SAFER_OBJECT_INFO_CLASS, SAFER_OBJECT_INFO_CLASS enumeration [Security], SaferObjectAllIdentificationGuids, SaferObjectDescription, SaferObjectExtendedError, SaferObjectFriendlyName, SaferObjectLevelId, SaferObjectScopeId, SaferObjectSingleIdentification, _SAFER_OBJECT_INFO_CLASS, security.safer_object_info_class, winsafer/SAFER_OBJECT_INFO_CLASS, winsafer/SaferObjectAllIdentificationGuids, winsafer/SaferObjectDescription, winsafer/SaferObjectExtendedError, winsafer/SaferObjectFriendlyName, winsafer/SaferObjectLevelId, winsafer/SaferObjectScopeId, winsafer/SaferObjectSingleIdentification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: VALENTW (Unicode) and VALENTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SAFER_OBJECT_INFO_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_OBJECT_INFO_CLASS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SAFER_OBJECT_INFO_CLASS enumeration


## -description


The <b>SAFER_OBJECT_INFO_CLASS</b> enumeration type defines the type of information requested about a Safer object.


## -enum-fields




### -field SaferObjectLevelId

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



The <b>SAFER_OBJECT_INFO_CLASS</b> enumeration type is used by the <a href="https://msdn.microsoft.com/cbe73ebc-bf2c-4d39-a203-78ff1a407481">SaferGetLevelInformation</a> function.



