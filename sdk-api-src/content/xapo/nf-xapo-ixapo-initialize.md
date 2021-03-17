---
UID: NF:xapo.IXAPO.Initialize
title: IXAPO::Initialize (xapo.h)
description: Performs any effect-specific initialization.
helpviewer_keywords: ["IXAPO interface [XAudio2 Audio Mixing APIs]","Initialize method","IXAPO.Initialize","IXAPO::Initialize","Initialize","Initialize method [XAudio2 Audio Mixing APIs]","Initialize method [XAudio2 Audio Mixing APIs]","IXAPO interface","xapo/IXAPO::Initialize","xaudio2.ixapo_interface_initialize"]
old-location: xaudio2\ixapo_interface_initialize.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.Initialize(const void,UINT32)
ms.date: 12/05/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],Initialize method, IXAPO.Initialize, IXAPO::Initialize, Initialize, Initialize method [XAudio2 Audio Mixing APIs], Initialize method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::Initialize, xaudio2.ixapo_interface_initialize
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
 - IXAPO::Initialize
 - xapo/IXAPO::Initialize
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
 - IXAPO.Initialize
---

# IXAPO::Initialize


## -description

Performs any effect-specific initialization.

## -parameters

### -param pData

Effect-specific initialization parameters, may be NULL if <i>DataByteSize</i> is 0.

### -param DataByteSize

Size of <i>pData</i> in bytes, may be 0 if <i>pData</i> is NULL.

## -returns

Returns S_OK if successful, an error code otherwise.

## -remarks

The contents of <i>pData</i> are defined by a given XAPO. Immutable parameters (constant for the lifetime of the XAPO) should be set in this method. Once initialized, an XAPO cannot be initialized again. An XAPO should be initialized before passing it to XAudio2 as part of an effect chain.



<div class="alert"><b>Note</b>  XAudio2 does not call this method, it should be called by the client before passing the XAPO to XAudio2.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>