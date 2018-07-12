---
UID: NF:d2d1_1helper.ConvertColorSpace
title: ConvertColorSpace function
author: windows-sdk-content
description: Convert a D2D1_COLOR_F from one color space to another.
old-location: direct2d\convertcolorspace.htm
old-project: direct2d
ms.assetid: 979E6FC2-52EB-4D58-B05C-523243F05B71
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: ConvertColorSpace, ConvertColorSpace function [Direct2D], d2d1_1helper/ConvertColorSpace, direct2d.convertcolorspace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D1_STROKE_STYLE_PROPERTIES1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ConvertColorSpace
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# ConvertColorSpace function


## -description


Convert a <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a> from one color space to another.


## -parameters




### -param sourceColorSpace

Type: <b><a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a></b>

The color space of the input.


### -param destinationColorSpace

Type: <b><a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a></b>

The desired color space of the output.


### -param color [ref]

Type: <b>const <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The input color.


## -returns



Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a></b>

The converted color in the new color space.



