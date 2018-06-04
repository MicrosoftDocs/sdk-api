---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

