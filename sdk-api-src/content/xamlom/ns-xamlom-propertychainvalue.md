---
UID: NS:xamlom.PropertyChainValue
title: PropertyChainValue
author: windows-sdk-content
description: Represents a property defined on an element.
old-location: xaml_diagnostics\propertychainvalue.htm
tech.root: xaml_diagnostics
ms.assetid: 111D10AB-2C16-4D21-A716-968C810B928F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PPropertyChainValue, PPropertyChainValue structure pointer, PropertyChainValue, PropertyChainValue structure, xaml_diagnostics.propertychainvalue, xamlom/PPropertyChainValue, xamlom/PropertyChainValue
ms.topic: struct
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xamlom.h
api_name:
 - PropertyChainValue
product: Windows
targetos: Windows
req.typenames: PropertyChainValue
req.redist: 
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

