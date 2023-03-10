---
UID: NF:audioengineendpoint.IAudioEndpoint.GetFramesPerPacket
title: IAudioEndpoint::GetFramesPerPacket (audioengineendpoint.h)
description: Gets the maximum number of frames per packet that the audio endpoint can support, based on the endpoint's period and the sample rate.
helpviewer_keywords: ["GetFramesPerPacket","GetFramesPerPacket method [Remote Desktop Services]","GetFramesPerPacket method [Remote Desktop Services]","IAudioEndpoint interface","IAudioEndpoint interface [Remote Desktop Services]","GetFramesPerPacket method","IAudioEndpoint.GetFramesPerPacket","IAudioEndpoint::GetFramesPerPacket","audioengineendpoint/IAudioEndpoint::GetFramesPerPacket","termserv.iaudioendpoint_getframesperpacket"]
old-location: termserv\iaudioendpoint_getframesperpacket.htm
tech.root: TermServ
ms.assetid: b9e47262-9e6f-4ddf-a74a-b7fa63983a5a
ms.date: 12/05/2018
ms.keywords: GetFramesPerPacket, GetFramesPerPacket method [Remote Desktop Services], GetFramesPerPacket method [Remote Desktop Services],IAudioEndpoint interface, IAudioEndpoint interface [Remote Desktop Services],GetFramesPerPacket method, IAudioEndpoint.GetFramesPerPacket, IAudioEndpoint::GetFramesPerPacket, audioengineendpoint/IAudioEndpoint::GetFramesPerPacket, termserv.iaudioendpoint_getframesperpacket
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpoint::GetFramesPerPacket
 - audioengineendpoint/IAudioEndpoint::GetFramesPerPacket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpoint.GetFramesPerPacket
---

# IAudioEndpoint::GetFramesPerPacket


## -description

The <b>GetFramesPerPacket</b> method gets the maximum number of frames per packet that the audio endpoint can support, based on the endpoint's period and the sample rate.

## -parameters

### -param pFramesPerPacket [out]

Receives the maximum number of frames per packet  that the endpoint can support.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpoint">IAudioEndpoint</a>