---
UID: NF:wingdi.SetColorSpace
title: SetColorSpace function (wingdi.h)
description: The SetColorSpace function defines the input color space for a given device context.
helpviewer_keywords: ["SetColorSpace","SetColorSpace function [Windows Color System]","_color_SetColorSpace","wcs.setcolorspace","wingdi/SetColorSpace"]
old-location: wcs\setcolorspace.htm
tech.root: WCS
ms.assetid: 037c864f-f8ec-4467-9236-74ea4493d743
ms.date: 12/05/2018
ms.keywords: SetColorSpace, SetColorSpace function [Windows Color System], _color_SetColorSpace, wcs.setcolorspace, wingdi/SetColorSpace
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetColorSpace
 - wingdi/SetColorSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetColorSpace
---

# SetColorSpace function


## -description

The <b>SetColorSpace</b> function defines the input [color space](/windows/win32/wcs/c#color-space) for a given device context.

## -parameters

### -param hdc

Specifies the handle to a device context.

### -param hcs

Identifies handle to the color space to set.

## -returns

If this function succeeds, the return value is a handle to the <i>hColorSpace</i> being replaced.

If this function fails, the return value is <b>NULL</b>.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
