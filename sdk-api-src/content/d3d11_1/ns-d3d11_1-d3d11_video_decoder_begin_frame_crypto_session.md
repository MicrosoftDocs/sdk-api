---
UID: NS:d3d11_1.D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
title: D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
author: windows-sdk-content
description: Provides data to the ID3D11VideoContext::DecoderBeginFrame method.
old-location: mf\d3d11_video_decoder_begin_frame_crypto_session.htm
old-project: medfound
ms.assetid: 7A4E0B99-90EE-4669-813E-5A3CD58D24A7
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION, D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION structure [Media Foundation], d3d11_1/D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION, mf.d3d11_video_decoder_begin_frame_crypto_session
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11_1.h
api_name:
-	D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_DECODER_BEGIN_FRAME_CRYPTO_SESSION structure


## -description


Provides data to the <a href="https://msdn.microsoft.com/395B06D8-1BCF-44F2-9F69-A183C30E36B7">ID3D11VideoContext::DecoderBeginFrame</a> method.


## -struct-fields




### -field pCryptoSession

A pointer to the ID3D11CryptoSession interface.  To get this pointer, call <a href="https://msdn.microsoft.com/1c0e3aa4-94d5-4398-a6c0-5466a437162d">ID3D11VideoDevice1::CreateCryptoSession</a>.


### -field BlobSize

The size of the memory buffer referenced by the <i>pBlob</i> member.


### -field pBlob

 


### -field pKeyInfoId

A pointer to a GUID identifying the hardware key.


### -field PrivateDataSize

The size of the memory buffer referenced by the <i>pPrivateData</i> member.


### -field pPrivateData

 




#### - VOID

The definition of this buffer is dependent on the implementation of the secure execution environment. It could contain a sealed key blob or any other per-key data that the secure execution environment needs to pass to the decode API.

The definition of this buffer is dependent on the implementation of the secure environment. It may contain data specific to the current frame.


## -remarks



This structure is passed in the <i>pContentKey</i> parameter of the <a href="https://msdn.microsoft.com/395B06D8-1BCF-44F2-9F69-A183C30E36B7">ID3D11VideoContext::DecoderBeginFrame</a> function when <a href="https://msdn.microsoft.com/CF2F3058-328A-4128-B5C6-29723B49AB1E">D3D11_DECODER_ENCRYPTION_HW_CENC</a>  is specified in the <b>guidConfigBitstreamEncryption</b> member of the <a href="https://msdn.microsoft.com/AB963FAD-F16C-47F6-8C78-FF4C234FBC60">D3D11_VIDEO_DECODER_CONFIG</a> structure when creating the video decoder interface.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

