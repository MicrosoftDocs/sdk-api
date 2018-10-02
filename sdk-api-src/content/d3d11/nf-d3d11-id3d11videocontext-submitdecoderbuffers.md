---
UID: NF:d3d11.ID3D11VideoContext.SubmitDecoderBuffers
title: ID3D11VideoContext::SubmitDecoderBuffers
author: windows-sdk-content
description: Submits one or more buffers for decoding.
old-location: mf\id3d11videocontext_submitdecoderbuffers.htm
tech.root: MedFound
ms.assetid: 39010E57-FFF2-4793-B839-E336E8D2C1B2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],SubmitDecoderBuffers method, ID3D11VideoContext.SubmitDecoderBuffers, ID3D11VideoContext::SubmitDecoderBuffers, SubmitDecoderBuffers, SubmitDecoderBuffers method [Media Foundation], SubmitDecoderBuffers method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::SubmitDecoderBuffers, mf.id3d11videocontext_submitdecoderbuffers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.SubmitDecoderBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::SubmitDecoderBuffers


## -description


Submits one or more buffers for decoding.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. To get this pointer, call the <a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">ID3D11VideoDevice::CreateVideoDecoder</a> method.


### -param NumBuffers [in]

The number of buffers submitted for decoding.


### -param pBufferDesc [in]

A pointer to an array of <a href="https://msdn.microsoft.com/B7F10FD2-79D1-483F-A95A-4CA7BAC7434F">D3D11_VIDEO_DECODER_BUFFER_DESC</a> structures. The <i>NumBuffers</i> parameter specifies the number of elements in the array. Each element in the array describes a compressed buffer for decoding.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function does not honor a D3D11 predicate that may have been set.

If the application uses <a href="https://msdn.microsoft.com/4161fbeb-7f58-422c-a195-ea10f737fd0c">D3D11 quries</a>, this function may not be accounted for with <b>D3D11_QUERY_EVENT</b> and <b>D3D11_QUERY_TIMESTAMP</b> when using feature levels lower than 11.  <b>D3D11_QUERY_PIPELINE_STATISTICS</b> will not include this function for any feature level.

When using feature levels 9_x, all partially encrypted buffers must use the same EncryptedBlockInfo, and partial encryption cannot be turned off on a per frame basis.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

