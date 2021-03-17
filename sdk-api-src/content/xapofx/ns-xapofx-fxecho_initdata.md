---
UID: NS:xapofx.FXECHO_INITDATA
title: FXECHO_INITDATA (xapofx.h)
description: Initialization parameters for use with the FXECHO XAPOFX.
helpviewer_keywords: ["FXECHO_INITDATA","FXECHO_INITDATA structure [XAudio2 Audio Mixing APIs]","xapofx/FXECHO_INITDATA","xaudio2.fxecho_initdata"]
old-location: xaudio2\fxecho_initdata.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapofx.FXECHO_INITDATA
ms.date: 12/05/2018
ms.keywords: FXECHO_INITDATA, FXECHO_INITDATA structure [XAudio2 Audio Mixing APIs], xapofx/FXECHO_INITDATA, xaudio2.fxecho_initdata
req.header: xapofx.h
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
req.typenames: FXECHO_INITDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FXECHO_INITDATA
 - xapofx/FXECHO_INITDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xapofx.h
api_name:
 - FXECHO_INITDATA
---

# FXECHO_INITDATA structure


## -description

Initialization parameters for use with the <a href="/windows/desktop/xaudio2/xapofx-overview">FXECHO XAPOFX</a>.

## -struct-fields

### -field MaxDelay

Maximum delay (all channels) in milliseconds. This must be within <b>FXECHO_MIN_DELAY</b> and <b>FXECHO_MAX_DELAY</b>.

## -remarks

Use of this structure is optional. The default <b>MaxDelay</b> is <b>FXECHO_DEFAULT_DELAY</b>.

<div class="alert"><b>Note</b>  The DirectX SDK versions of XAUDIO2 don't support this functionality.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>