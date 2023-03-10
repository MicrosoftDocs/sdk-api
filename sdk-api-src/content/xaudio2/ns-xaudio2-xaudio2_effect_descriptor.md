---
UID: NS:xaudio2.XAUDIO2_EFFECT_DESCRIPTOR
title: XAUDIO2_EFFECT_DESCRIPTOR (xaudio2.h)
description: Contains information about an XAPO for use in an effect chain.
helpviewer_keywords: ["XAUDIO2_EFFECT_DESCRIPTOR","XAUDIO2_EFFECT_DESCRIPTOR structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_effect_descriptor","xaudio2/XAUDIO2_EFFECT_DESCRIPTOR"]
old-location: xaudio2\xaudio2_effect_descriptor.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_EFFECT_DESCRIPTOR
ms.date: 12/05/2018
ms.keywords: XAUDIO2_EFFECT_DESCRIPTOR, XAUDIO2_EFFECT_DESCRIPTOR structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_effect_descriptor, xaudio2/XAUDIO2_EFFECT_DESCRIPTOR
req.header: xaudio2.h
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
req.typenames: XAUDIO2_EFFECT_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_EFFECT_DESCRIPTOR
 - xaudio2/XAUDIO2_EFFECT_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_EFFECT_DESCRIPTOR
---

# XAUDIO2_EFFECT_DESCRIPTOR structure


## -description

Contains information about an <a href="/windows/desktop/xaudio2/xapo-overview">XAPO</a> for use in an effect chain.

## -struct-fields

### -field pEffect

Pointer to the <b>IUnknown</b> interface of the <a href="/windows/desktop/xaudio2/xapo-overview">XAPO</a> object.

### -field InitialState

TRUE if the effect should begin in the enabled state. Otherwise, FALSE.

### -field OutputChannels

Number of output channels the effect should produce.

## -remarks

XAPO instances are passed to XAudio2 as <b>IUnknown</b> interfaces and XAudio2 uses <a href="/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)">IXAPO::QueryInterface</a> to acquire an <a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a> interface and to detect whether the XAPO implements the <a href="/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a> interface.



For additional information on using XAPOs with XAudio2 see <a href="/windows/desktop/xaudio2/how-to--create-an-effect-chain">How to: Create an Effect Chain</a> and <a href="/windows/desktop/xaudio2/how-to--use-an-xapo-in-xaudio2">How to: Use an XAPO in XAudio2</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>



<a href="/windows/desktop/xaudio2/structures">XAudio2 Structures</a>



<a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAudio2_Effect_Chain</a>