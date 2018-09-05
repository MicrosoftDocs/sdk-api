---
UID: NF:windows.graphics.imaging.interop.ISoftwareBitmapNativeFactory.CreateFromWICBitmap
title: ISoftwareBitmapNativeFactory::imaging
author: windows-sdk-content
description: Creates an ISoftwareBitmapNative from the provided IWICBitmap.
old-location: winrt\isoftwarebitmapnativefactory_createfromwicbitmap.htm
old-project: WinRT
ms.assetid: D52F70E8-AF26-40A5-8E9E-1A5B9D20E35F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateFromWICBitmap, CreateFromWICBitmap method [Windows Runtime], CreateFromWICBitmap method [Windows Runtime],ISoftwareBitmapNativeFactory interface, ISoftwareBitmapNativeFactory interface [Windows Runtime],CreateFromWICBitmap method, ISoftwareBitmapNativeFactory.CreateFromWICBitmap, ISoftwareBitmapNativeFactory.imaging, ISoftwareBitmapNativeFactory::CreateFromWICBitmap, ISoftwareBitmapNativeFactory::imaging, windows/ISoftwareBitmapNativeFactory::CreateFromWICBitmap, winrt.isoftwarebitmapnativefactory_createfromwicbitmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: windows.graphics.imaging.interop.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.graphics.imaging.interop.dll
api_name:
 - ISoftwareBitmapNativeFactory.CreateFromWICBitmap
product: Windows
targetos: Windows
req.lib: Windows.graphics.imaging.interop.lib
req.dll: Windows.graphics.imaging.interop.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISoftwareBitmapNativeFactory::imaging


## -description


Creates an <a href="https://msdn.microsoft.com/9EB9C74E-A056-4A40-AFAD-0056E139BA28">ISoftwareBitmapNative</a>  from the provided <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a>.


## -parameters




### -param data [in]

Type: <b>IWICBitmap*</b>

The source WIC bitmap.


### -param forceReadOnly [in]

Type: <b>BOOL</b>

A value indicating whether the created software bitmap is read-only.

<div class="alert"><b>Note</b>  The read-only access applies only to the Windows Runtime<a href="https://msdn.microsoft.com/cf4130af-344e-454e-ab61-a8238db94a06">SoftwareBitmap</a> wrapper. Access to the underlying Media Foundation buffer is not restricted.</div>
<div> </div>

### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="https://msdn.microsoft.com/9EB9C74E-A056-4A40-AFAD-0056E139BA28">ISoftwareBitmapNative</a> interface.


### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://msdn.microsoft.com/613BFE81-AC55-4786-B6BD-0FFB7506D7F1">ISoftwareBitmapNativeFactory</a>
 

 

