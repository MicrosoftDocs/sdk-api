---
UID: NE:xamlom.MetadataBit
title: MetadataBit (xamlom.h)
description: Defines constants that are used to define the PropertyChainValue returned from XAML Diagnostics.
old-location: xaml_diagnostics\metadatabit.htm
tech.root: xaml_diagnostics
ms.assetid: 951A4C1F-B176-4D18-821A-CEAD1116B8BE
ms.date: 12/05/2018
ms.keywords: IsPropertyReadOnly, IsValueBindingExpression, IsValueCollection, IsValueCollectionReadOnly, IsValueHandle, IsValueHandleAndEvaluatedValue, IsValueNull, MatadataBit, MatadataBit enumeration, MetadataBit, None, xaml_diagnostics.metadatabit, xamlom/IsPropertyReadOnly, xamlom/IsValueBindingExpression, xamlom/IsValueCollection, xamlom/IsValueCollectionReadOnly, xamlom/IsValueHandle, xamlom/IsValueHandleAndEvaluatedValue, xamlom/IsValueNull, xamlom/MatadataBit, xamlom/None
f1_keywords:
- xamlom/MetadataBit
dev_langs:
- c++
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
- MetadataBit
targetos: Windows
req.typenames: MetadataBit
req.redist: 
ms.custom: 19H1
---

# MetadataBit enumeration


## -description


Defines constants that are used to define the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/ns-xamlom-propertychainvalue">PropertyChainValue</a> returned from XAML Diagnostics.


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

