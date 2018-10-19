---
UID: NF:d2d1_1helper.PrintControlProperties
title: PrintControlProperties function
author: windows-sdk-content
description: Returns a filled D2D1_PRINT_CONTROL_PROPERTIES structure.
old-location: direct2d\printcontrolproperties.htm
tech.root: direct2d
ms.assetid: 0AD341B6-DA74-417B-9F2F-20557B090F49
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: PrintControlProperties, PrintControlProperties function [Direct2D], d2d1_1helper/PrintControlProperties, direct2d.printcontrolproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - PrintControlProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PrintControlProperties function


## -description


Returns a filled <a href="https://msdn.microsoft.com/en-us/library/Hh847949(v=VS.85).aspx">D2D1_PRINT_CONTROL_PROPERTIES</a> structure.


## -parameters




### -param fontSubsetMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh871442(v=VS.85).aspx">D2D1_PRINT_FONT_SUBSET_MODE</a></b>

The mode to use for selecting fonts for printing.


### -param rasterDpi

Type: <b>FLOAT</b>

DPI for rasterization of all unsupported D2D commands or options, defaults to150.0


### -param colorSpace

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh446992(v=VS.85).aspx">D2D1_COLOR_SPACE</a></b>

Color space for vector graphics in XPS package


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh847949(v=VS.85).aspx">D2D1_PRINT_CONTROL_PROPERTIES</a></b>

The creation properties for a <a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a> object.



