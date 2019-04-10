---
UID: NF:dwrite_1.IDWriteBitmapRenderTarget1.SetTextAntialiasMode
title: IDWriteBitmapRenderTarget1::SetTextAntialiasMode (dwrite_1.h)
author: windows-sdk-content
description: Sets the current text antialiasing mode of the bitmap render target.
old-location: directwrite\idwritebitmaprendertarget1_settextantialiasmode.htm
tech.root: DirectWrite
ms.assetid: 813C984D-81BC-4CAA-8C0A-166612E8028F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteBitmapRenderTarget1 interface [Direct Write],SetTextAntialiasMode method, IDWriteBitmapRenderTarget1.SetTextAntialiasMode, IDWriteBitmapRenderTarget1::SetTextAntialiasMode, SetTextAntialiasMode, SetTextAntialiasMode method [Direct Write], SetTextAntialiasMode method [Direct Write],IDWriteBitmapRenderTarget1 interface, directwrite.idwritebitmaprendertarget1_settextantialiasmode, dwrite_1/IDWriteBitmapRenderTarget1::SetTextAntialiasMode
ms.topic: method
req.header: dwrite_1.h
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
 - IDWriteBitmapRenderTarget1.SetTextAntialiasMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteBitmapRenderTarget1::SetTextAntialiasMode


## -description


Sets the current text antialiasing mode of the bitmap render target.


## -parameters




### -param antialiasMode

Type: <b><a href="https://msdn.microsoft.com/212B02C9-1265-4870-A059-F292640ECE15">DWRITE_TEXT_ANTIALIAS_MODE</a></b>

A <a href="https://msdn.microsoft.com/212B02C9-1265-4870-A059-F292640ECE15">DWRITE_TEXT_ANTIALIAS_MODE</a>-typed value that specifies the antialiasing mode.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or E_INVALIDARG if the argument is not valid.




## -remarks



The antialiasing mode of a newly-created bitmap render target defaults to 
     <a href="https://msdn.microsoft.com/en-us/library/JJ127237(v=VS.85).aspx">DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE</a>. An app can change the antialiasing
     mode by calling <b>SetTextAntialiasMode</b>. For example, an app might specify
    <a href="https://msdn.microsoft.com/en-us/library/JJ127237(v=VS.85).aspx">DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE</a> for grayscale antialiasing when it renders text onto a transparent bitmap.




## -see-also




<a href="https://msdn.microsoft.com/5A7D2723-932B-4707-ABCC-0C0282FB7A56">IDWriteBitmapRenderTarget1</a>
 

 

