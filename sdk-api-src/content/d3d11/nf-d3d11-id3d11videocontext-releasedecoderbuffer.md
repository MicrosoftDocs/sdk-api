---
UID: NF:d3d11.ID3D11VideoContext.ReleaseDecoderBuffer
title: ID3D11VideoContext::ReleaseDecoderBuffer
author: windows-sdk-content
description: Releases a buffer that was obtained by calling the ID3D11VideoContext::GetDecoderBuffer method.
old-location: mf\id3d11videocontext_releasedecoderbuffer.htm
tech.root: medfound
ms.assetid: C7BD4CA6-706D-4C3A-AED1-EDF1C65E41E0
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],ReleaseDecoderBuffer method, ID3D11VideoContext.ReleaseDecoderBuffer, ID3D11VideoContext::ReleaseDecoderBuffer, ReleaseDecoderBuffer, ReleaseDecoderBuffer method [Media Foundation], ReleaseDecoderBuffer method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::ReleaseDecoderBuffer, mf.id3d11videocontext_releasedecoderbuffer
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
 - ID3D11VideoContext.ReleaseDecoderBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::ReleaseDecoderBuffer


## -description


Releases a buffer that was obtained by calling the <a href="https://msdn.microsoft.com/6842D5D7-6165-4428-91BD-2234BE5332B8">ID3D11VideoContext::GetDecoderBuffer</a> method.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">ID3D11VideoDevice::CreateVideoDecoder</a>.


### -param Type [in]

The type of buffer to release. Specify the same value that was used in the <i>Type</i> parameter of the <a href="https://msdn.microsoft.com/6842D5D7-6165-4428-91BD-2234BE5332B8">GetDecoderBuffer</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

