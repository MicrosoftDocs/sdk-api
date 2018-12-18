---
UID: NF:d2d1_1.ID2D1Bitmap1.Map
title: ID2D1Bitmap1::Map
author: windows-sdk-content
description: Maps the given bitmap into memory.
old-location: direct2d\id2d1bitmap1_map.htm
tech.root: direct2d
ms.assetid: 284c16ea-1a9f-4f13-b359-214178650add
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1Bitmap1 interface [Direct2D],Map method, ID2D1Bitmap1.Map, ID2D1Bitmap1::Map, Map, Map method [Direct2D], Map method [Direct2D],ID2D1Bitmap1 interface, d2d1_1/ID2D1Bitmap1::Map, direct2d.id2d1bitmap1_map
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Bitmap1.Map
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Bitmap1::Map


## -description


Maps  the given bitmap into memory.


## -parameters




### -param options

Type: <b><a href="https://msdn.microsoft.com/8706c3e3-eb29-4760-bdfd-f19afc6f2bf7">D2D1_MAP_OPTIONS</a></b>

The options used in mapping the bitmap into memory.


### -param mappedRect [out]

Type: <b><a href="https://msdn.microsoft.com/1cd81f1a-c39b-4975-a801-aa9444dde172">D2D1_MAPPED_RECT</a>*</b>

When this method returns, contains a reference to the rectangle that is mapped into memory.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One or more arguments are not valid</td>
</tr>
<tr>
<td>D3DERR_DEVICELOST</td>
<td>The device has been lost but cannot be reset at this time.</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  You can't use bitmaps for some purposes while mapped. Particularly, the <a href="https://msdn.microsoft.com/d43685d9-292c-462c-bdd2-c4e81b6d704e">ID2D1Bitmap::CopyFromBitmap</a> method doesn't work if either the source or destination bitmap is mapped.</div>
<div> </div>
The bitmap must have been created with the <b>D2D1_BITMAP_OPTIONS_CPU_READ</b> flag specified.




## -see-also




<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>



<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>



<a href="https://msdn.microsoft.com/76d49be7-b0ac-44a7-aeaf-a7b18346a2bf">ID2D1DeviceContext::CreateBitmapFromDxgiSurface</a>



<a href="https://msdn.microsoft.com/c6377dbd-ffd9-458b-9e03-5a832f095818">ID2D1RenderTarget::CreateSharedBitmap</a>
 

 

