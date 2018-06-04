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

# _CENTRAL_ACCESS_POLICY_ENTRY structure


## -description


Represents a central access policy entry containing a list of security descriptors and staged security descriptors.


## -struct-fields




### -field Name

The name of the central access policy entry.


### -field Description

The description of the central access policy entry.


### -field ChangeId

An identifier that can be used to version the central access policy entry.


### -field LengthAppliesTo

The length of the buffer pointed to by the <i>AppliesTo</i> field.


### -field AppliesTo

A resource condition in binary form.


### -field LengthSD

The length of the buffer pointed to by the <i>SD</i> field.


### -field SD

A buffer of security descriptors associated with the entry.


### -field LengthStagedSD

The length of the buffer pointed to by the <i>StagedSD</i> field.


### -field StagedSD

A buffer of staged security descriptors associated with the entry.


### -field Flags

This field is reserved.

