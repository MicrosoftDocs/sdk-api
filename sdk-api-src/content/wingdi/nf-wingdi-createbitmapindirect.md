---
UID: NF:wingdi.CreateBitmapIndirect
title: CreateBitmapIndirect function (wingdi.h)
description: The CreateBitmapIndirect function creates a bitmap with the specified width, height, and color format (color planes and bits-per-pixel).
helpviewer_keywords: ["CreateBitmapIndirect","CreateBitmapIndirect function [Windows GDI]","_win32_CreateBitmapIndirect","gdi.createbitmapindirect","wingdi/CreateBitmapIndirect"]
old-location: gdi\createbitmapindirect.htm
tech.root: gdi
ms.assetid: 79f73e28-4ee3-472d-9a20-3ffe7cf2a6b5
ms.date: 12/05/2018
ms.keywords: CreateBitmapIndirect, CreateBitmapIndirect function [Windows GDI], _win32_CreateBitmapIndirect, gdi.createbitmapindirect, wingdi/CreateBitmapIndirect
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
 - CreateBitmapIndirect
 - wingdi/CreateBitmapIndirect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - CreateBitmapIndirect
---

# CreateBitmapIndirect function


## -description

The <b>CreateBitmapIndirect</b> function creates a bitmap with the specified width, height, and color format (color planes and bits-per-pixel).

## -parameters

### -param pbm [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a> structure that contains information about the bitmap. If an application sets the <b>bmWidth</b> or <b>bmHeight</b> members to zero, <b>CreateBitmapIndirect</b> returns the handle to a 1-by-1 pixel, monochrome bitmap.

## -returns

If the function succeeds, the return value is a handle to the bitmap.

If the function fails, the return value is <b>NULL</b>.

This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The bitmap is too big for memory to be allocated.

</td>
</tr>
</table>

## -remarks

The <b>CreateBitmapIndirect</b> function creates a device-dependent bitmap.

After a bitmap is created, it can be selected into a device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function. However, the bitmap can only be selected into a device context if the bitmap and the DC have the same format.

While the <b>CreateBitmapIndirect</b> function can be used to create color bitmaps, for performance reasons applications should use <b>CreateBitmapIndirect</b> to create monochrome bitmaps and <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a> to create color bitmaps. Whenever a color bitmap from <b>CreateBitmapIndirect</b> is selected into a device context, the system must ensure that the bitmap matches the format of the device context it is being selected into. Because <b>CreateCompatibleBitmap</b> takes a device context, it returns a bitmap that has the same format as the specified device context. Thus, subsequent calls to <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> are faster with a color bitmap from <b>CreateCompatibleBitmap</b> than with a color bitmap returned from <b>CreateBitmapIndirect</b>.

If the bitmap is monochrome, zeros represent the foreground color and ones represent the background color for the destination device context.

When you no longer need the bitmap, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmap">CreateBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>