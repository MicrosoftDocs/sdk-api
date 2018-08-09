---
UID: NS:xamlom.VisualElement
title: VisualElement
author: windows-sdk-content
description: Represents a XAML element in the Live Visual Tree in Microsoft Visual Studio.
old-location: xaml_diagnostics\visualelement.htm
old-project: xaml_diagnostics
ms.assetid: 655642E7-64B3-439A-BAE1-7D54461EE058
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: PVisualElement, PVisualElement structure pointer, VisualElement, VisualElement structure, xaml_diagnostics.visualelement, xamlom/PVisualElement, xamlom/VisualElement
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VisualElement
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xamlom.h
api_name:
 - VisualElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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

The name of the XAML element, if it has an <a href="https://msdn.microsoft.com/4FF1F3ED-903A-4305-B2BD-DCD29E0C9E6D">x:Name</a> defined in markup.


### -field NumChildren

The number of children the XAML element has.

