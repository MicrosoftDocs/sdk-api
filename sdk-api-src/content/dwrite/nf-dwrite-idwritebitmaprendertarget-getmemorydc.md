---
UID: NF:dwrite.IDWriteBitmapRenderTarget.GetMemoryDC
title: IDWriteBitmapRenderTarget::GetMemoryDC
author: windows-sdk-content
description: Gets a handle to the memory device context.
old-location: directwrite\IDWriteBitmapRenderTarget_GetMemoryDC.htm
tech.root: DirectWrite
ms.assetid: 9ca9a002-2a78-4c7c-926c-52414dd801bb
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetMemoryDC, GetMemoryDC method [Direct Write], GetMemoryDC method [Direct Write],IDWriteBitmapRenderTarget interface, IDWriteBitmapRenderTarget interface [Direct Write],GetMemoryDC method, IDWriteBitmapRenderTarget.GetMemoryDC, IDWriteBitmapRenderTarget::GetMemoryDC, directwrite.IDWriteBitmapRenderTarget_GetMemoryDC, dwrite/IDWriteBitmapRenderTarget::GetMemoryDC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteBitmapRenderTarget.GetMemoryDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteBitmapRenderTarget::GetMemoryDC


## -description


 Gets a handle to the memory device context.


## -parameters






## -returns



Type: <b>HDC</b>

Returns a device context handle to the memory device context.




## -remarks



 An application can use the device context to draw using GDI functions. An application can obtain the bitmap handle
     (HBITMAP) by calling <a href="https://msdn.microsoft.com/d7e2310c-6a9e-4195-824c-1a83382a5c5b">GetCurrentObject</a>. An application that wants information about the underlying bitmap, including
     a pointer to the pixel data, can call <a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a> to fill in a <a href="https://msdn.microsoft.com/76e84c90-6553-46c6-9ab9-afa022e0b2e5">DIBSECTION</a> structure. The bitmap is always a 32-bit 
     top-down DIB.

Note that this method takes no parameters and returns an HDC variable, not an HRESULT.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>memoryHdc = g_pBitmapRenderTarget-&gt;GetMemoryDC();
</pre>
</td>
</tr>
</table></span></div>
The HDC returned here is still owned by the bitmap render targer object and should not be released or deleted by the client.




## -see-also




<a href="https://msdn.microsoft.com/9953a9e9-7772-41a3-9cd9-2340a9dd4b6f">IDWriteBitmapRenderTarget</a>
 

 

