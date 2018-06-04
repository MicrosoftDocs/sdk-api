---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



