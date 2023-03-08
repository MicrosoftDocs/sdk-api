---
UID: NN:strmif.IAMAudioRendererStats
title: IAMAudioRendererStats (strmif.h)
description: The IAMAudioRendererStats interface retrieves statistical performance information from an audio renderer filter.This interface is intended for use during development, to log performance data from the audio renderer.
helpviewer_keywords: ["IAMAudioRendererStats","IAMAudioRendererStats interface [DirectShow]","IAMAudioRendererStats interface [DirectShow]","described","IAMAudioRendererStatsInterface","dshow.iamaudiorendererstats","strmif/IAMAudioRendererStats"]
old-location: dshow\iamaudiorendererstats.htm
tech.root: dshow
ms.assetid: f5cca658-73ce-4f4d-8992-afb7824f4117
ms.date: 12/05/2018
ms.keywords: IAMAudioRendererStats, IAMAudioRendererStats interface [DirectShow], IAMAudioRendererStats interface [DirectShow],described, IAMAudioRendererStatsInterface, dshow.iamaudiorendererstats, strmif/IAMAudioRendererStats
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMAudioRendererStats
 - strmif/IAMAudioRendererStats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAudioRendererStats
---

# IAMAudioRendererStats interface


## -description

The <code>IAMAudioRendererStats</code> interface retrieves statistical performance information from an audio renderer filter.

This interface is intended for use during development, to log performance data from the audio renderer. There is probably no reason for an application to use it in a retail build. The <a href="/windows/desktop/DirectShow/audio-renderer--waveout--filter">Audio Renderer (WaveOut)</a> filter and the <a href="/windows/desktop/DirectShow/directsound-renderer-filter">DirectSound Renderer</a> filter both expose this interface.

<b>Filter Developers</b>: It is not expected that other filters will implement this interface.

## -inheritance

The <b>IAMAudioRendererStats</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMAudioRendererStats</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
