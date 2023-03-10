---
UID: NS:xamlom.PropertyChainValue
title: PropertyChainValue (xamlom.h)
description: Represents a property defined on an element.
helpviewer_keywords: ["PPropertyChainValue","PPropertyChainValue structure pointer","PropertyChainValue","PropertyChainValue structure","xaml_diagnostics.propertychainvalue","xamlom/PPropertyChainValue","xamlom/PropertyChainValue"]
old-location: xaml_diagnostics\propertychainvalue.htm
tech.root: xaml_diagnostics
ms.assetid: 111D10AB-2C16-4D21-A716-968C810B928F
ms.date: 12/05/2018
ms.keywords: PPropertyChainValue, PPropertyChainValue structure pointer, PropertyChainValue, PropertyChainValue structure, xaml_diagnostics.propertychainvalue, xamlom/PPropertyChainValue, xamlom/PropertyChainValue
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
targetos: Windows
req.typenames: PropertyChainValue
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PropertyChainValue
 - xamlom/PropertyChainValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xamlom.h
api_name:
 - PropertyChainValue
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

The value of the property.  (Represents an <b>InstanceHandle</b> if <a href="/previous-versions/windows/desktop/api/xamlom/ne-xamlom-metadatabit">MetadataBit</a> is set.)

### -field Overridden

Indicates whether the property is overridden by some property in the value chain.

### -field MetadataBits

A bit field that represents <a href="/previous-versions/windows/desktop/api/xamlom/ne-xamlom-metadatabit">MetadataBit</a>s.

### -field PropertyName

The name of the property.

### -field PropertyChainIndex

The index in the <a href="/previous-versions/windows/desktop/api/xamlom/ns-xamlom-propertychainsource">PropertyChainSource</a> returned by GetPropertyValuesChain
that represents the source of this property.