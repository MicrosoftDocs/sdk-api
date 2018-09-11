---
UID: NF:wincodec.IWICBitmapFrameEncode.GetMetadataQueryWriter
title: IWICBitmapFrameEncode::GetMetadataQueryWriter
author: windows-sdk-content
description: Gets the metadata query writer for the encoder frame.
old-location: wic\_wic_codec_iwicbitmapframeencode_getmetadataquerywriter.htm
tech.root: wic
ms.assetid: 0ff79820-5f44-4262-b97f-df783829e44b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMetadataQueryWriter, GetMetadataQueryWriter method [Windows Imaging Component], GetMetadataQueryWriter method [Windows Imaging Component],IWICBitmapFrameEncode interface, IWICBitmapFrameEncode interface [Windows Imaging Component],GetMetadataQueryWriter method, IWICBitmapFrameEncode.GetMetadataQueryWriter, IWICBitmapFrameEncode::GetMetadataQueryWriter, _wic_codec_iwicbitmapframeencode_getmetadataquerywriter, wic._wic_codec_iwicbitmapframeencode_getmetadataquerywriter, wincodec/IWICBitmapFrameEncode::GetMetadataQueryWriter
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICBitmapFrameEncode.GetMetadataQueryWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapFrameEncode::GetMetadataQueryWriter


## -description


Gets the metadata query writer for the encoder frame.


## -parameters




### -param ppIMetadataQueryWriter [out]

Type: <b><a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to metadata query writer for the encoder frame.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you are setting metadata on the frame, you must do this before you use <a href="https://msdn.microsoft.com/6b430fe0-5230-47dc-95c0-aeabd138cefe">IWICBitmapFrameEncode::WritePixels</a> or <a href="https://msdn.microsoft.com/bc748982-6dc8-41cc-a23b-9d127dc22a1f">IWICBitmapFrameEncode::WriteSource</a> to write any image pixels to the frame




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a7cfaa6d-e17d-458a-ae63-72963615bef8">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

