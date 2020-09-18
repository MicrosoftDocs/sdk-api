---
UID: NF:d2d1_1helper.PrintControlProperties
title: PrintControlProperties function (d2d1_1helper.h)
description: Returns a filled D2D1_PRINT_CONTROL_PROPERTIES structure.
helpviewer_keywords: ["PrintControlProperties","PrintControlProperties function [Direct2D]","d2d1_1helper/PrintControlProperties","direct2d.printcontrolproperties"]
old-location: direct2d\printcontrolproperties.htm
tech.root: Direct2D
ms.assetid: 0AD341B6-DA74-417B-9F2F-20557B090F49
ms.date: 12/05/2018
ms.keywords: PrintControlProperties, PrintControlProperties function [Direct2D], d2d1_1helper/PrintControlProperties, direct2d.printcontrolproperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PrintControlProperties
 - d2d1_1helper/PrintControlProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - PrintControlProperties
---

# PrintControlProperties function


## -description

Returns a filled <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_print_control_properties">D2D1_PRINT_CONTROL_PROPERTIES</a> structure.

## -parameters

### -param fontSubsetMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode">D2D1_PRINT_FONT_SUBSET_MODE</a></b>

The mode to use for selecting fonts for printing.

### -param rasterDpi

Type: <b>FLOAT</b>

DPI for rasterization of all unsupported D2D commands or options, defaults to150.0

### -param colorSpace

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

Color space for vector graphics in XPS package

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_print_control_properties">D2D1_PRINT_CONTROL_PROPERTIES</a></b>

The creation properties for a <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a> object.