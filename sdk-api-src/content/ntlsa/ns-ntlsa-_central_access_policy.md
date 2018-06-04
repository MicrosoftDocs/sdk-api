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

# _CENTRAL_ACCESS_POLICY structure


## -description


Represents a central access policy that contains a set of central access policy entries.


## -struct-fields




### -field CAPID

The identifier of the central access policy.


### -field Name

The name of the central access policy.


### -field Description

The description of the central access policy.


### -field ChangeId

An identifier that can be used to version the central access policy.


### -field Flags

Reserved.


### -field CAPECount

The length of the buffer pointed to by the <i>CAPEs</i> field.


### -field CAPEs

Pointer to a buffer of <a href="https://msdn.microsoft.com/8667848D-096C-422E-B4A6-38CC406F0F4A">CENTRAL_ACCESS_POLICY_ENTRY</a> pointers.

