---
UID: NF:wingdi.CreateBitmapIndirect
title: CreateBitmapIndirect function
author: windows-sdk-content
description: The CreateBitmapIndirect function creates a bitmap with the specified width, height, and color format (color planes and bits-per-pixel).
old-location: gdi\createbitmapindirect.htm
tech.root: gdi
ms.assetid: 79f73e28-4ee3-472d-9a20-3ffe7cf2a6b5
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateBitmapIndirect, CreateBitmapIndirect function [Windows GDI], _win32_CreateBitmapIndirect, gdi.createbitmapindirect, wingdi/CreateBitmapIndirect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateBitmapIndirect function


## -description


The <b>CreateBitmapIndirect</b> function creates a bitmap with the specified width, height, and color format (color planes and bits-per-pixel).


## -parameters




### -param pbm [in]

A pointer to a <a href="https://msdn.microsoft.com/6ee382da-dd63-442b-80c3-59472defb41f">BITMAP</a> structure that contains information about the bitmap. If an application sets the <b>bmWidth</b> or <b>bmHeight</b> members to zero, <b>CreateBitmapIndirect</b> returns the handle to a 1-by-1 pixel, monochrome bitmap.


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

After a bitmap is created, it can be selected into a device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function. However, the bitmap can only be selected into a device context if the bitmap and the DC have the same format.

While the <b>CreateBitmapIndirect</b> function can be used to create color bitmaps, for performance reasons applications should use <b>CreateBitmapIndirect</b> to create monochrome bitmaps and <a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a> to create color bitmaps. Whenever a color bitmap from <b>CreateBitmapIndirect</b> is selected into a device context, the system must ensure that the bitmap matches the format of the device context it is being selected into. Because <b>CreateCompatibleBitmap</b> takes a device context, it returns a bitmap that has the same format as the specified device context. Thus, subsequent calls to <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> are faster with a color bitmap from <b>CreateCompatibleBitmap</b> than with a color bitmap returned from <b>CreateBitmapIndirect</b>.

If the bitmap is monochrome, zeros represent the foreground color and ones represent the background color for the destination device context.

When you no longer need the bitmap, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.




## -see-also




<a href="https://msdn.microsoft.com/6ee382da-dd63-442b-80c3-59472defb41f">BITMAP</a>



<a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a>



<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/b52e1baf-6a81-44bc-a061-4d42e6f4ed64">CreateBitmap</a>



<a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a>



<a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

