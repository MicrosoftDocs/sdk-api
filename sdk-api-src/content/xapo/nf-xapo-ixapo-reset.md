---
UID: NF:xapo.IXAPO.Reset
title: IXAPO::Reset (xapo.h)
description: Resets variables dependent on frame history.
helpviewer_keywords: ["IXAPO interface [XAudio2 Audio Mixing APIs]","Reset method","IXAPO.Reset","IXAPO::Reset","Reset","Reset method [XAudio2 Audio Mixing APIs]","Reset method [XAudio2 Audio Mixing APIs]","IXAPO interface","xapo/IXAPO::Reset","xaudio2.ixapo_interface_reset"]
old-location: xaudio2\ixapo_interface_reset.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.Reset
ms.date: 12/05/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],Reset method, IXAPO.Reset, IXAPO::Reset, Reset, Reset method [XAudio2 Audio Mixing APIs], Reset method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::Reset, xaudio2.ixapo_interface_reset
req.header: xapo.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAPO::Reset
 - xapo/IXAPO::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.Reset
---

# IXAPO::Reset


## -description

Resets variables dependent on frame history.



## -remarks

Constant and locked parameters such as the input and output formats remain unchanged. Variables set by <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a> remain unchanged.



For example, an effect with delay should zero out its delay line during this method, but should not reallocate anything as the XAPO remains locked with a constant input and output configuration.



XAudio2 only calls this method if the XAPO is locked.



This method is called from the realtime thread and should not block.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>
