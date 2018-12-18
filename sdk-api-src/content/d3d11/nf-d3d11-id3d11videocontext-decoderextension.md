---
UID: NF:d3d11.ID3D11VideoContext.DecoderExtension
title: ID3D11VideoContext::DecoderExtension
author: windows-sdk-content
description: Performs an extended function for decoding.
old-location: mf\id3d11videocontext_decoderextension.htm
tech.root: medfound
ms.assetid: B96FD793-C82A-4752-8F59-3CC9B86D1C2D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DecoderExtension, DecoderExtension method [Media Foundation], DecoderExtension method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],DecoderExtension method, ID3D11VideoContext.DecoderExtension, ID3D11VideoContext::DecoderExtension, d3d11/ID3D11VideoContext::DecoderExtension, mf.id3d11videocontext_decoderextension
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ID3D11VideoContext.DecoderExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::DecoderExtension


## -description


Performs an extended function for decoding. This method enables extensions to the basic decoder functionality.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">ID3D11VideoDevice::CreateVideoDecoder</a>.


### -param pExtensionData [in]

A pointer to a <a href="https://msdn.microsoft.com/F82746A4-16AB-49B5-96C8-777675416467">D3D11_VIDEO_DECODER_EXTENSION</a> structure that contains data for the function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

