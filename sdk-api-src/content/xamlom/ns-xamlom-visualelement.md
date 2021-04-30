---
UID: NS:xamlom.VisualElement
title: VisualElement (xamlom.h)
description: Represents a XAML element in the Live Visual Tree in Microsoft Visual Studio.
helpviewer_keywords: ["PVisualElement","PVisualElement structure pointer","VisualElement","VisualElement structure","xaml_diagnostics.visualelement","xamlom/PVisualElement","xamlom/VisualElement"]
old-location: xaml_diagnostics\visualelement.htm
tech.root: xaml_diagnostics
ms.assetid: 655642E7-64B3-439A-BAE1-7D54461EE058
ms.date: 12/05/2018
ms.keywords: PVisualElement, PVisualElement structure pointer, VisualElement, VisualElement structure, xaml_diagnostics.visualelement, xamlom/PVisualElement, xamlom/VisualElement
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
req.typenames: VisualElement
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VisualElement
 - xamlom/VisualElement
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
 - VisualElement
---

# VisualElement structure


## -description

Represents a XAML element in the Live Visual Tree in Microsoft Visual Studio.

## -struct-fields

### -field Handle

A handle to the object.

### -field SrcInfo

Information about the XAML source document.

### -field Type

The type of the object.

### -field Name

The name of the XAML element, if it has an <a href="/windows/uwp/xaml-platform/x-name-attribute">x:Name</a> defined in markup.

### -field NumChildren

The number of children the XAML element has.