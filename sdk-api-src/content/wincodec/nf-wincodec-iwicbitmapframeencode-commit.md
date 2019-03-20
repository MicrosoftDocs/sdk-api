---
UID: NF:wincodec.IWICBitmapFrameEncode.Commit
title: IWICBitmapFrameEncode::Commit (wincodec.h)
author: windows-sdk-content
description: Commits the frame to the image.
old-location: wic\_wic_codec_iwicbitmapframeencode_commit.htm
tech.root: wic
ms.assetid: 6321fb9e-9ea8-423c-a332-9daa589af6f7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Commit, Commit method [Windows Imaging Component], Commit method [Windows Imaging Component],IWICBitmapFrameEncode interface, IWICBitmapFrameEncode interface [Windows Imaging Component],Commit method, IWICBitmapFrameEncode.Commit, IWICBitmapFrameEncode::Commit, _wic_codec_iwicbitmapframeencode_commit, wic._wic_codec_iwicbitmapframeencode_commit, wincodec/IWICBitmapFrameEncode::Commit
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
 - IWICBitmapFrameEncode.Commit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapFrameEncode::Commit


## -description


Commits the frame to the image.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After the frame <b>Commit</b> has been called, you can't use or reinitialize the <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> object and any objects created from it.


To finalize the image, both the frame <b>Commit</b> and the encoder <a href="https://msdn.microsoft.com/97e39e73-3494-4679-8962-eb48242f9b9f">Commit</a> must be called. However, only call the encoder  <b>Commit</b> method after all frames have been committed.




## -see-also




<a href="https://msdn.microsoft.com/97e39e73-3494-4679-8962-eb48242f9b9f">Commit</a>



<a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>
 

 

