---
UID: NF:wincodec.IWICBitmapSource.CopyPalette
title: IWICBitmapSource::CopyPalette
author: windows-sdk-content
description: Retrieves the color table for indexed pixel formats.
old-location: wic\_wic_codec_iwicbitmapsource_copypalette.htm
tech.root: wic
ms.assetid: 5e45ca4a-2d14-4829-9542-9cfc3e4b0d73
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CopyPalette, CopyPalette method [Windows Imaging Component], CopyPalette method [Windows Imaging Component],IWICBitmapSource interface, IWICBitmapSource interface [Windows Imaging Component],CopyPalette method, IWICBitmapSource.CopyPalette, IWICBitmapSource::CopyPalette, _wic_codec_iwicbitmapsource_copypalette, wic._wic_codec_iwicbitmapsource_copypalette, wincodec/IWICBitmapSource::CopyPalette
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapSource.CopyPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapSource::CopyPalette


## -description


Retrieves the color table for indexed pixel formats.


## -parameters




### -param pIPalette [in]

Type: <b><a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>*</b>

An <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>. A palette can be created using the <a href="https://msdn.microsoft.com/135440ee-ea70-40da-9ee1-618a8e10170a">CreatePalette</a> method.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINCODEC_ERR_PALETTEUNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The palette was unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The palette was successfully copied.

</td>
</tr>
</table>
 




## -remarks



If the <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> is an <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a>, the function may return the image's global palette if a frame-level palette is not available.
            The global palette may also be retrieved using the <a href="https://msdn.microsoft.com/4a387936-b045-42c7-b57c-1ac470640a14">CopyPalette</a> method.
         



