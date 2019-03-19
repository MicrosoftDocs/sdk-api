---
UID: NF:wincodec.IWICBitmapEncoder.Commit
title: IWICBitmapEncoder::Commit (wincodec.h)
author: windows-sdk-content
description: Commits all changes for the image and closes the stream.
old-location: wic\_wic_codec_iwicbitmapencoder_commit.htm
tech.root: wic
ms.assetid: 97e39e73-3494-4679-8962-eb48242f9b9f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Commit, Commit method [Windows Imaging Component], Commit method [Windows Imaging Component],IWICBitmapEncoder interface, IWICBitmapEncoder interface [Windows Imaging Component],Commit method, IWICBitmapEncoder.Commit, IWICBitmapEncoder::Commit, _wic_codec_iwicbitmapencoder_commit, wic._wic_codec_iwicbitmapencoder_commit, wincodec/IWICBitmapEncoder::Commit
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
 - IWICBitmapEncoder.Commit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapEncoder::Commit


## -description


Commits all changes for the image and closes the stream.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To finalize an image, both the frame <a href="https://msdn.microsoft.com/6321fb9e-9ea8-423c-a332-9daa589af6f7">Commit</a> and the encoder <b>Commit</b> must be called. However, only call the encoder  <b>Commit</b> method after all frames have been committed.

After the encoder has been committed, it can't be re-initialized or reused with another stream. A new encoder interface must be created, for example, with <a href="https://msdn.microsoft.com/7aae3ea6-2d8b-4764-9c78-a6cce49012a5">IWICImagingFactory::CreateEncoder</a>.


For the encoder <b>Commit</b> to succeed, you must at a minimum call  <a href="https://msdn.microsoft.com/60a7e0b8-202c-4fed-b105-f8c4fa9817a9">IWICBitmapEncoder::Initialize</a> and either <a href="https://msdn.microsoft.com/bc748982-6dc8-41cc-a23b-9d127dc22a1f">IWICBitmapFrameEncode::WriteSource</a> or <a href="https://msdn.microsoft.com/6b430fe0-5230-47dc-95c0-aeabd138cefe">IWICBitmapFrameEncode::WritePixels</a>.



<a href="https://msdn.microsoft.com/bc748982-6dc8-41cc-a23b-9d127dc22a1f">IWICBitmapFrameEncode::WriteSource</a> specifies all parameters needed to encode the image data. <a href="https://msdn.microsoft.com/6b430fe0-5230-47dc-95c0-aeabd138cefe">IWICBitmapFrameEncode::WritePixels</a> requires that you also call <a href="https://msdn.microsoft.com/e21e1a66-b1fa-4700-a14e-dc382b5404f7">IWICBitmapFrameEncode::SetSize</a>, <a href="https://msdn.microsoft.com/9327b5dd-18a3-40c6-8bb4-245fcc7fb582">IWICBitmapFrameEncode::SetPixelFormat</a>, and <a href="https://msdn.microsoft.com/c463fc95-695d-4ba3-bf62-5b09d69c60c2">IWICBitmapFrameEncode::SetPalette</a> (if the pixel format is indexed).





## -see-also




<a href="https://msdn.microsoft.com/6321fb9e-9ea8-423c-a332-9daa589af6f7">Commit</a>



<a href="https://msdn.microsoft.com/fe87c9ae-dedf-4ec2-ac11-0ea5fc6aa3ad">IWICBitmapEncoder</a>
 

 

