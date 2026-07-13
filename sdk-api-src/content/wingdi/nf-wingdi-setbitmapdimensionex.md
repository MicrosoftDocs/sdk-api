---
UID: NF:wingdi.SetBitmapDimensionEx
title: SetBitmapDimensionEx function (wingdi.h)
description: The SetBitmapDimensionEx function assigns preferred dimensions to a bitmap. These dimensions can be used by applications; however, they are not used by the system.
helpviewer_keywords: ["SetBitmapDimensionEx","SetBitmapDimensionEx function [Windows GDI]","_win32_SetBitmapDimensionEx","gdi.setbitmapdimensionex","wingdi/SetBitmapDimensionEx"]
old-location: gdi\setbitmapdimensionex.htm
tech.root: gdi
ms.assetid: 23960533-de71-4bff-a43f-75e5fe38fbec
ms.date: 12/05/2018
ms.keywords: SetBitmapDimensionEx, SetBitmapDimensionEx function [Windows GDI], _win32_SetBitmapDimensionEx, gdi.setbitmapdimensionex, wingdi/SetBitmapDimensionEx
req.header: wingdi.h
req.include-header: Windows.h
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
 - SetBitmapDimensionEx
 - wingdi/SetBitmapDimensionEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetBitmapDimensionEx
---

# SetBitmapDimensionEx function


## -description

The <b>SetBitmapDimensionEx</b> function assigns preferred dimensions to a bitmap. These dimensions can be used by applications; however, they are not used by the system.

## -parameters

### -param hbm [in]

A handle to the bitmap. The bitmap cannot be a DIB-section bitmap.

### -param w [in]

The width, in 0.1-millimeter units, of the bitmap.

### -param h [in]

The height, in 0.1-millimeter units, of the bitmap.

### -param lpsz [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure to receive the previous dimensions of the bitmap. This pointer can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

An application can retrieve the dimensions assigned to a bitmap with the <b>SetBitmapDimensionEx</b> function by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getbitmapdimensionex">GetBitmapDimensionEx</a> function.

The bitmap identified by <i>hBitmap</i> cannot be a DIB section, which is a bitmap created by the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a> function. If the bitmap is a DIB section, the <b>SetBitmapDimensionEx</b> function fails.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbitmapdimensionex">GetBitmapDimensionEx</a>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>