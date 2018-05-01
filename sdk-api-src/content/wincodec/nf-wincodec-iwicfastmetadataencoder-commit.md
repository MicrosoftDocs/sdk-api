---
UID: NF:wincodec.IWICFastMetadataEncoder.Commit
title: IWICFastMetadataEncoder::Commit method
author: windows-driver-content
description: Finalizes metadata changes to the image stream.
old-location: wic\_wic_codec_iwicfastmetadataencoder_commit.htm
old-project: wic
ms.assetid: 24f3b0f8-8991-4f55-aeb6-a2bbf09a29c7
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Commit method [Windows Imaging Component], Commit method [Windows Imaging Component], IWICFastMetadataEncoder interface, Commit,IWICFastMetadataEncoder.Commit, IWICFastMetadataEncoder, IWICFastMetadataEncoder interface [Windows Imaging Component], Commit method, IWICFastMetadataEncoder::Commit, _wic_codec_iwicfastmetadataencoder_commit, wic._wic_codec_iwicfastmetadataencoder_commit, wincodec/IWICFastMetadataEncoder::Commit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICFastMetadataEncoder.Commit
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICFastMetadataEncoder::Commit method


## -description


Finalizes metadata changes to the image stream.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the commit fails and returns <b>WINCODEC_ERR_STREAMNOTAVAILABLE</b>, ensure that the image decoder was loaded using the <b>WICDecodeMetadataCacheOnDemand</b> option. A fast metadata encoder is not supported when the decoder is created using the <b>WICDecodeMetadataCacheOnLoad</b> option. 

If the commit fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.



