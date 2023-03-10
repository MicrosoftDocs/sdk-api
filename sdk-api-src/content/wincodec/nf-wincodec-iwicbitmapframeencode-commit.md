---
UID: NF:wincodec.IWICBitmapFrameEncode.Commit
title: IWICBitmapFrameEncode::Commit (wincodec.h)
description: Commits the frame to the image.
helpviewer_keywords: ["Commit","Commit method [Windows Imaging Component]","Commit method [Windows Imaging Component]","IWICBitmapFrameEncode interface","IWICBitmapFrameEncode interface [Windows Imaging Component]","Commit method","IWICBitmapFrameEncode.Commit","IWICBitmapFrameEncode::Commit","_wic_codec_iwicbitmapframeencode_commit","wic._wic_codec_iwicbitmapframeencode_commit","wincodec/IWICBitmapFrameEncode::Commit"]
old-location: wic\_wic_codec_iwicbitmapframeencode_commit.htm
tech.root: wic
ms.assetid: 6321fb9e-9ea8-423c-a332-9daa589af6f7
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Windows Imaging Component], Commit method [Windows Imaging Component],IWICBitmapFrameEncode interface, IWICBitmapFrameEncode interface [Windows Imaging Component],Commit method, IWICBitmapFrameEncode.Commit, IWICBitmapFrameEncode::Commit, _wic_codec_iwicbitmapframeencode_commit, wic._wic_codec_iwicbitmapframeencode_commit, wincodec/IWICBitmapFrameEncode::Commit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapFrameEncode::Commit
 - wincodec/IWICBitmapFrameEncode::Commit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameEncode.Commit
---

# IWICBitmapFrameEncode::Commit


## -description

Commits the frame to the image.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After the frame <b>Commit</b> has been called, you can't use or reinitialize the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a> object and any objects created from it.


To finalize the image, both the frame <b>Commit</b> and the encoder <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapencoder-commit">Commit</a> must be called. However, only call the encoder  <b>Commit</b> method after all frames have been committed.

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapencoder-commit">Commit</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>
