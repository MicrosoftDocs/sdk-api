---
UID: NF:wingdi.DeleteColorSpace
title: DeleteColorSpace function (wingdi.h)
description: The DeleteColorSpace function removes and destroys a specified color space.
helpviewer_keywords: ["DeleteColorSpace","DeleteColorSpace function [Windows Color System]","_color_DeleteColorSpace","wcs.deletecolorspace","wingdi/DeleteColorSpace"]
old-location: wcs\deletecolorspace.htm
tech.root: WCS
ms.assetid: 5b241224-2994-4533-9629-d2a4b129ce86
ms.date: 12/05/2018
ms.keywords: DeleteColorSpace, DeleteColorSpace function [Windows Color System], _color_DeleteColorSpace, wcs.deletecolorspace, wingdi/DeleteColorSpace
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
 - DeleteColorSpace
 - wingdi/DeleteColorSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
 - GDI32Min.dll
api_name:
 - DeleteColorSpace
---

# DeleteColorSpace function


## -description

The <b>DeleteColorSpace</b> function removes and destroys a specified [color space](/windows/win32/wcs/c#color-space).

## -parameters

### -param hcs

Specifies the handle to a color space to delete.

## -returns

If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
