---
UID: NF:d3d11.ID3D11VideoContext.DecoderEndFrame
title: ID3D11VideoContext::DecoderEndFrame
author: windows-sdk-content
description: Signals the end of a decoding operation.
old-location: mf\id3d11videocontext_decoderendframe.htm
tech.root: MedFound
ms.assetid: 3596B70C-4BED-49C4-A0E4-8702DA219B01
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: DecoderEndFrame, DecoderEndFrame method [Media Foundation], DecoderEndFrame method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],DecoderEndFrame method, ID3D11VideoContext.DecoderEndFrame, ID3D11VideoContext::DecoderEndFrame, d3d11/ID3D11VideoContext::DecoderEndFrame, mf.id3d11videocontext_decoderendframe
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
 - ID3D11VideoContext.DecoderEndFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::DecoderEndFrame


## -description


Signals the end of a decoding operation.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">ID3D11VideoDevice::CreateVideoDecoder</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>



<a href="https://msdn.microsoft.com/395B06D8-1BCF-44F2-9F69-A183C30E36B7">ID3D11VideoContext::DecoderBeginFrame</a>
 

 

