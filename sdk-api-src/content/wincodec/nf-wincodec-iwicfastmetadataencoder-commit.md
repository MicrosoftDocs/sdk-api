---
UID: NF:wincodec.IWICFastMetadataEncoder.Commit
title: IWICFastMetadataEncoder::Commit (wincodec.h)
description: Finalizes metadata changes to the image stream.
helpviewer_keywords: ["Commit","Commit method [Windows Imaging Component]","Commit method [Windows Imaging Component]","IWICFastMetadataEncoder interface","IWICFastMetadataEncoder interface [Windows Imaging Component]","Commit method","IWICFastMetadataEncoder.Commit","IWICFastMetadataEncoder::Commit","_wic_codec_iwicfastmetadataencoder_commit","wic._wic_codec_iwicfastmetadataencoder_commit","wincodec/IWICFastMetadataEncoder::Commit"]
old-location: wic\_wic_codec_iwicfastmetadataencoder_commit.htm
tech.root: wic
ms.assetid: 24f3b0f8-8991-4f55-aeb6-a2bbf09a29c7
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Windows Imaging Component], Commit method [Windows Imaging Component],IWICFastMetadataEncoder interface, IWICFastMetadataEncoder interface [Windows Imaging Component],Commit method, IWICFastMetadataEncoder.Commit, IWICFastMetadataEncoder::Commit, _wic_codec_iwicfastmetadataencoder_commit, wic._wic_codec_iwicfastmetadataencoder_commit, wincodec/IWICFastMetadataEncoder::Commit
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
 - IWICFastMetadataEncoder::Commit
 - wincodec/IWICFastMetadataEncoder::Commit
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
 - IWICFastMetadataEncoder.Commit
---

# IWICFastMetadataEncoder::Commit


## -description

Finalizes metadata changes to the image stream.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the commit fails and returns <b>WINCODEC_ERR_STREAMNOTAVAILABLE</b>, ensure that the image decoder was loaded using the <b>WICDecodeMetadataCacheOnDemand</b> option. A fast metadata encoder is not supported when the decoder is created using the <b>WICDecodeMetadataCacheOnLoad</b> option. 

If the commit fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.

