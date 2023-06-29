---
UID: NF:effects.IWMPEffects.SetCurrentPreset
title: IWMPEffects::SetCurrentPreset (effects.h)
description: The SetCurrentPreset method gets the current preset from Windows Media Player and sets it in the visualization.
helpviewer_keywords: ["EffectsSetCurrentPreset","IWMPEffects interface [Windows Media Player]","SetCurrentPreset method","IWMPEffects.SetCurrentPreset","IWMPEffects::SetCurrentPreset","SetCurrentPreset","SetCurrentPreset method [Windows Media Player]","SetCurrentPreset method [Windows Media Player]","IWMPEffects interface","effects/IWMPEffects::SetCurrentPreset","wmp.iwmpeffects_setcurrentpreset"]
old-location: wmp\iwmpeffects_setcurrentpreset.htm
tech.root: WMP
ms.assetid: 090e5f9b-e7f1-48b6-9018-3d0797493d42
ms.date: 4/26/2023
ms.keywords: EffectsSetCurrentPreset, IWMPEffects interface [Windows Media Player],SetCurrentPreset method, IWMPEffects.SetCurrentPreset, IWMPEffects::SetCurrentPreset, SetCurrentPreset, SetCurrentPreset method [Windows Media Player], SetCurrentPreset method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::SetCurrentPreset, wmp.iwmpeffects_setcurrentpreset
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
 - IWMPEffects::SetCurrentPreset
 - effects/IWMPEffects::SetCurrentPreset
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
 - IWMPEffects.SetCurrentPreset
---

# IWMPEffects::SetCurrentPreset


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetCurrentPreset</b> method gets the current preset from Windows Media Player and sets it in the visualization.

## -parameters

### -param nPreset [out]

<b>Long</b> value specifying the new preset index.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This is called by the Windows Media Player to request that the given preset be displayed.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>