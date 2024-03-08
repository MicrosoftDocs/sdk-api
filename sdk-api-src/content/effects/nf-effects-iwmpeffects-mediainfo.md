---
UID: NF:effects.IWMPEffects.MediaInfo
title: IWMPEffects::MediaInfo (effects.h)
description: The MediaInfo method sends channel and sample rate data to the visualization.
helpviewer_keywords: ["EffectsMediaInfo","IWMPEffects interface [Windows Media Player]","MediaInfo method","IWMPEffects.MediaInfo","IWMPEffects::MediaInfo","MediaInfo","MediaInfo method [Windows Media Player]","MediaInfo method [Windows Media Player]","IWMPEffects interface","effects/IWMPEffects::MediaInfo","wmp.iwmpeffects_mediainfo"]
old-location: wmp\iwmpeffects_mediainfo.htm
tech.root: WMP
ms.assetid: 1267cb11-1b45-4f38-ad3c-02213405ed66
ms.date: 4/26/2023
ms.keywords: EffectsMediaInfo, IWMPEffects interface [Windows Media Player],MediaInfo method, IWMPEffects.MediaInfo, IWMPEffects::MediaInfo, MediaInfo, MediaInfo method [Windows Media Player], MediaInfo method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::MediaInfo, wmp.iwmpeffects_mediainfo
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later.
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
 - IWMPEffects::MediaInfo
 - effects/IWMPEffects::MediaInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects.MediaInfo
---

# IWMPEffects::MediaInfo


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MediaInfo</b> method sends channel and sample rate data to the visualization.

## -parameters

### -param lChannelCount [in]

<b>Long</b> integer containing the number of channels (one for mono, or two for stereo).

### -param lSampleRate [in]

<b>Long</b> integer containing the sample rate in hertz (Hz). For example, a value of 22500 would specify a rate of 22.5KHz.

### -param bstrTitle [in]

<b>String</b> specifying the title.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>