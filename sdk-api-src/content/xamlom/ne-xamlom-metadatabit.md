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

# MetadataBit enumeration


## -description


Defines constants that are used to define the <a href="https://msdn.microsoft.com/111D10AB-2C16-4D21-A716-968C810B928F">PropertyChainValue</a> returned from XAML Diagnostics.


## -enum-fields




### -field None

No special bits are set.


### -field IsValueHandle

The value represents a string representation of an <b>InstanceHandle</b>.


### -field IsPropertyReadOnly

The property is read only and cannot be set locally.


### -field IsValueCollection

The value represents a collection object. (When set, <b>IsValueHandle</b> is also set.)


### -field IsValueCollectionReadOnly

The value represents a read only collection.


### -field IsValueBindingExpression

The value represents the evaluated value of a binding expression.


### -field IsValueNull

The value is <b>null</b>. (Introduced in Windows 10, version 1607.)


### -field IsValueHandleAndEvaluatedValue

The value represents a string representation of an <b>InstanceHandle</b> and an evaluated value. (Introduced in Windows 10, version 1607.)

