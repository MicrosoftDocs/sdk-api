---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush1)
title: ID2D1DeviceContext::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush1)
author: windows-sdk-content
description: Creates a bitmap brush, the input image is a Direct2D bitmap object.
old-location: direct2d\id2d1devicecontext_createbitmapbrush.htm
tech.root: direct2d
ms.assetid: E6385DBD-1A3B-4504-9987-35258E90DBC7
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CreateBitmapBrush, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateBitmapBrush method, ID2D1DeviceContext.CreateBitmapBrush, ID2D1DeviceContext.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush1), ID2D1DeviceContext::CreateBitmapBrush, ID2D1DeviceContext::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush1), d2d1_1/ID2D1DeviceContext::CreateBitmapBrush, direct2d.id2d1devicecontext_createbitmapbrush
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1DeviceContext.CreateBitmapBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush1)


## -description


Creates a bitmap brush, the input image is a Direct2D bitmap object.


## -parameters




### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap to use as the brush.


### -param bitmapBrushProperties [in, optional]

Type: <b><a href="https://msdn.microsoft.com/0FECAD03-C35C-4729-9BBE-40DE11B34068">D2D1_BITMAP_BRUSH_PROPERTIES1</a>*</b>

A bitmap brush properties structure.


#### - brushProperties [in, optional]

Type: <b><a href="https://msdn.microsoft.com/37b2fc18-a320-41c0-8717-dcd561a2f2df">D2D1_BRUSH_PROPERTIES</a>*</b>

A brush properties structure.


### -param bitmapBrush [out]

Type: <b><a href="https://msdn.microsoft.com/5EF60CF5-DB7E-4453-80A2-F248A82A37E3">ID2D1BitmapBrush1</a>**</b>

The address of the newly created bitmap brush object.


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
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0FECAD03-C35C-4729-9BBE-40DE11B34068">D2D1_BITMAP_BRUSH_PROPERTIES1</a>



<a href="https://msdn.microsoft.com/9c3be6a0-ac67-4dc1-9c5a-0ee47343cb86">D2D1_BRUSH_PROPERTIES</a>



<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>



<a href="https://msdn.microsoft.com/5EF60CF5-DB7E-4453-80A2-F248A82A37E3">ID2D1BitmapBrush1</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

