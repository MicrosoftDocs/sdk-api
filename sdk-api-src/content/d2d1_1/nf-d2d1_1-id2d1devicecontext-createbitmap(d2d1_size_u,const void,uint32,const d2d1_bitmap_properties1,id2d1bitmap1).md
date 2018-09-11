---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1,ID2D1Bitmap1)
title: ID2D1DeviceContext::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1,ID2D1Bitmap1)
author: windows-sdk-content
description: Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the DrawBitmap and ID2D1BitmapBrush APIs. In addition, color context information can be passed to the bitmap.
old-location: direct2d\id2d1devicecontext_createbitmap.htm
tech.root: direct2d
ms.assetid: 8292da6b-8232-4ef0-967d-a53d586aa9a9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateBitmap, CreateBitmap method [Direct2D], CreateBitmap method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateBitmap method, ID2D1DeviceContext.CreateBitmap, ID2D1DeviceContext.CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1,ID2D1Bitmap1), ID2D1DeviceContext::CreateBitmap, ID2D1DeviceContext::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1,ID2D1Bitmap1), d2d1_1/ID2D1DeviceContext::CreateBitmap, direct2d.id2d1devicecontext_createbitmap
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
 - ID2D1DeviceContext.CreateBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1,ID2D1Bitmap1)


## -description


Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the <a href="https://msdn.microsoft.com/e6cff1b7-055b-442c-99aa-afeeee4d06e8">DrawBitmap</a> and <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> APIs. In addition, color context information can be passed to the bitmap.


## -parameters




### -param size

Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a></b>

The pixel size of the bitmap to be created.


### -param sourceData

TBD


### -param pitch

Type: <b>UINT32</b>

The pitch of the source data, if specified.


### -param bitmapProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/c9371ce3-f6fc-4fe6-ada6-0aa64a8f29a2">D2D1_BITMAP_PROPERTIES1</a>*</b>

The properties of the bitmap to be created.


### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>**</b>

When this method returns, contains the address of a pointer to a new bitmap object.


#### - srcData [in, optional]

Type: <b>const void*</b>

The initial data that will be loaded into the bitmap.


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
<td>An invalid value was passed to the method.</td>
</tr>
<tr>
<td>D3DERR_OUTOFVIDEOMEMORY</td>
<td>Direct3D does not have enough display memory to perform the operation.</td>
</tr>
</table>
 




## -remarks



The new bitmap can be used as a target for <a href="https://msdn.microsoft.com/66914048-7bef-4551-bb14-5ab67c727dc5">SetTarget</a> if it is created with <a href="https://msdn.microsoft.com/c080e23e-99c4-46ed-8b21-be26dec288af">D2D1_BITMAP_OPTIONS_TARGET</a>.




## -see-also




<a href="https://msdn.microsoft.com/c9371ce3-f6fc-4fe6-ada6-0aa64a8f29a2">D2D1_BITMAP_PROPERTIES1</a>



<a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a>



<a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

