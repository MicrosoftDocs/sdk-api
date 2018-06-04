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

# PropertyChainValue structure


## -description


Represents a property defined on an element.


## -struct-fields




### -field Index

The index of property in the XAML runtime.


### -field Type

The type of the object.


### -field DeclaringType

The base type of the object.


### -field ValueType

The type of the current value of the property.


### -field ItemType

Collection item type, or <b>null</b> if not a collection.


### -field Value

The value of the property.  (Represents an <b>InstanceHandle</b> if <a href="https://msdn.microsoft.com/951A4C1F-B176-4D18-821A-CEAD1116B8BE">MetadataBit</a> is set.)


### -field Overridden

Indicates whether the property is overridden by some property in the value chain.


### -field MetadataBits

A bit field that represents <a href="https://msdn.microsoft.com/951A4C1F-B176-4D18-821A-CEAD1116B8BE">MetadataBit</a>s.


### -field PropertyName

The name of the property.


### -field PropertyChainIndex

The index in the <a href="https://msdn.microsoft.com/B9A506D5-5F7B-429C-AA62-52B4C5BF78E0">PropertyChainSource</a> returned by GetPropertyValuesChain
that represents the source of this property.

