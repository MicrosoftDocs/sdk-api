---
UID: NS:xamlom.PropertyChainSource
title: PropertyChainSource
author: windows-sdk-content
description: Represents the source object (a Style) of a target type.
old-location: xaml_diagnostics\propertychainsource.htm
old-project: xaml_diagnostics
ms.assetid: B9A506D5-5F7B-429C-AA62-52B4C5BF78E0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PPropertyChainSource, PPropertyChainSource structure pointer, PropertyChainSource, PropertyChainSource structure, xaml_diagnostics.propertychainsource, xamlom/PPropertyChainSource, xamlom/PropertyChainSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xamlom.h
req.include-header: 
req.redist: 
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
req.typenames: PropertyChainSource
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xamlom.h
api_name:
 - PropertyChainSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# PropertyChainSource structure


## -description


Represents the source object (a <a href="https://msdn.microsoft.com/745e7a38-841e-4bcc-893b-51577d8811c2">Style</a>) of a target type.


## -struct-fields




### -field Handle

A handle to the style.


### -field TargetType

The target type of the style, defined in markup.


### -field Name

The name of the style, if it has an <a href="https://msdn.microsoft.com/4FF1F3ED-903A-4305-B2BD-DCD29E0C9E6D">x:Name</a> defined in markup.


### -field Source

Where the style is defined in the application .


### -field SrcInfo

 




#### - srcInfo

Source information about where the style is defined.

