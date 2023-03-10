---
UID: NF:d2d1_1.ID2D1Bitmap1.Unmap
title: ID2D1Bitmap1::Unmap (d2d1_1.h)
description: Unmaps the bitmap from memory.
helpviewer_keywords: ["ID2D1Bitmap1 interface [Direct2D]","Unmap method","ID2D1Bitmap1.Unmap","ID2D1Bitmap1::Unmap","Unmap","Unmap method [Direct2D]","Unmap method [Direct2D]","ID2D1Bitmap1 interface","d2d1_1/ID2D1Bitmap1::Unmap","direct2d.id2d1bitmap1_unmap"]
old-location: direct2d\id2d1bitmap1_unmap.htm
tech.root: Direct2D
ms.assetid: 471c6e8a-4412-4efc-a7bf-688b1da7e367
ms.date: 12/05/2018
ms.keywords: ID2D1Bitmap1 interface [Direct2D],Unmap method, ID2D1Bitmap1.Unmap, ID2D1Bitmap1::Unmap, Unmap, Unmap method [Direct2D], Unmap method [Direct2D],ID2D1Bitmap1 interface, d2d1_1/ID2D1Bitmap1::Unmap, direct2d.id2d1bitmap1_unmap
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Bitmap1::Unmap
 - d2d1_1/ID2D1Bitmap1::Unmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Bitmap1.Unmap
---

# ID2D1Bitmap1::Unmap


## -description

Unmaps the bitmap from memory.



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
<td>One or more arguments are not valid.</td>
</tr>
<tr>
<td>E_POINTER</td>
<td>Pointer is not valid.</td>
</tr>
</table>

## -remarks

Any memory returned from the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map">Map</a> call is now invalid and may be reclaimed by the operating system or used for other purposes. 

The bitmap must have been previously mapped.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options">D2D1_BITMAP_OPTIONS</a>



<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_mapped_rect">D2D1_MAPPED_RECT</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>
