---
UID: NN:rdpencomapi.IRDPSRAPIAudioStream
title: IRDPSRAPIAudioStream (rdpencomapi.h)
description: Enables sending an audio stream from the collaboration sharer Microsoft ActiveX control to collaboration viewer controls.
helpviewer_keywords: ["IRDPSRAPIAudioStream","IRDPSRAPIAudioStream class [RDP]","IRDPSRAPIAudioStream class [RDP]","described","rdp.irdpsrapiaudiostream","rdpencomapi/IRDPSRAPIAudioStream"]
old-location: rdp\irdpsrapiaudiostream.htm
tech.root: rdp
ms.assetid: B2BC04A1-DE22-4543-9F10-33B0B99E0F92
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAudioStream, IRDPSRAPIAudioStream class [RDP], IRDPSRAPIAudioStream class [RDP],described, rdp.irdpsrapiaudiostream, rdpencomapi/IRDPSRAPIAudioStream
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIAudioStream
 - rdpencomapi/IRDPSRAPIAudioStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAudioStream
---

# IRDPSRAPIAudioStream interface


## -description

Enables sending an audio stream from the collaboration sharer Microsoft ActiveX control to 
    collaboration viewer controls. This interface only supports a pulse code modulation (PCM) audio stream 
    with the following specifications; 44.1 kHz, 2 channels, 16 bits/sample.

## -inheritance

The <b>IRDPSRAPIAudioStream</b> class inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRDPSRAPIAudioStream</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/rdp/windows-desktop-sharing-interfaces">Windows Desktop Sharing Interfaces</a>
