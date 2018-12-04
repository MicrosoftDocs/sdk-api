---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1)
title: ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1)
author: windows-sdk-content
description: Creates a Direct2D bitmap by copying a WIC bitmap.
old-location: direct2d\id2d1devicecontext_createbitmapfromwicbitmap2.htm
tech.root: direct2d
ms.assetid: 74CB0A1C-2103-4C43-87C7-50C55057424D
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: CreateBitmapFromWicBitmap, CreateBitmapFromWicBitmap method [Direct2D], CreateBitmapFromWicBitmap method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateBitmapFromWicBitmap method, ID2D1DeviceContext.CreateBitmapFromWicBitmap, ID2D1DeviceContext.CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1), ID2D1DeviceContext::CreateBitmapFromWicBitmap, ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1), d2d1_1/ID2D1DeviceContext::CreateBitmapFromWicBitmap, direct2d.id2d1devicecontext_createbitmapfromwicbitmap2
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
 - ID2D1DeviceContext.CreateBitmapFromWicBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1)


## -description


Creates a Direct2D bitmap by copying a WIC bitmap.


## -parameters




### -param wicBitmapSource [in]

Type: <b><a href="https://msdn.microsoft.com/98BA78CD-4902-43B9-A412-895CA2A112C7">IWICBitmapSource</a>*</b>

The WIC bitmap source to copy from.


### -param bitmapProperties [in, ref, optional]

Type: <b>const <a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">D2D1_BITMAP_PROPERTIES1</a></b>

A bitmap properties structure that specifies bitmap creation options.


### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>**</b>

The address of the newly created bitmap object.


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




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

