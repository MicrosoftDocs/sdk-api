---
UID: NS:xamlom.PropertyChainSource
title: PropertyChainSource (xamlom.h)
description: Represents the source object (a Style) of a target type.
helpviewer_keywords: ["PPropertyChainSource","PPropertyChainSource structure pointer","PropertyChainSource","PropertyChainSource structure","xaml_diagnostics.propertychainsource","xamlom/PPropertyChainSource","xamlom/PropertyChainSource"]
old-location: xaml_diagnostics\propertychainsource.htm
tech.root: xaml_diagnostics
ms.assetid: B9A506D5-5F7B-429C-AA62-52B4C5BF78E0
ms.date: 12/05/2018
ms.keywords: PPropertyChainSource, PPropertyChainSource structure pointer, PropertyChainSource, PropertyChainSource structure, xaml_diagnostics.propertychainsource, xamlom/PPropertyChainSource, xamlom/PropertyChainSource
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
req.typenames: PropertyChainSource
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PropertyChainSource
 - xamlom/PropertyChainSource
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
 - PropertyChainSource
---

# PropertyChainSource structure


## -description

Represents the source object (a <a href="/uwp/api/windows.ui.xaml.style">Style</a>) of a target type.

## -struct-fields

### -field Handle

A handle to the style.

### -field TargetType

The target type of the style, defined in markup.

### -field Name

The name of the style, if it has an <a href="/windows/uwp/xaml-platform/x-name-attribute">x:Name</a> defined in markup.

### -field Source

Where the style is defined in the application .

### -field SrcInfo

### -field srcInfo

Source information about where the style is defined.