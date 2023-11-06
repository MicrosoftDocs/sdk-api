---
UID: NF:effects.IWMPEffects.GetCapabilities
title: IWMPEffects::GetCapabilities (effects.h)
description: The GetCapabilities method gets the capabilities of the visualization.
helpviewer_keywords: ["EffectsGetCapabilities","GetCapabilities","GetCapabilities method [Windows Media Player]","GetCapabilities method [Windows Media Player]","IWMPEffects interface","IWMPEffects interface [Windows Media Player]","GetCapabilities method","IWMPEffects.GetCapabilities","IWMPEffects::GetCapabilities","effects/IWMPEffects::GetCapabilities","wmp.iwmpeffects_getcapabilities"]
old-location: wmp\iwmpeffects_getcapabilities.htm
tech.root: WMP
ms.assetid: e2efb0cd-417f-4b96-a4d7-c02c41a6244d
ms.date: 4/26/2023
ms.keywords: EffectsGetCapabilities, GetCapabilities, GetCapabilities method [Windows Media Player], GetCapabilities method [Windows Media Player],IWMPEffects interface, IWMPEffects interface [Windows Media Player],GetCapabilities method, IWMPEffects.GetCapabilities, IWMPEffects::GetCapabilities, effects/IWMPEffects::GetCapabilities, wmp.iwmpeffects_getcapabilities
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later
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
 - IWMPEffects::GetCapabilities
 - effects/IWMPEffects::GetCapabilities
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
 - IWMPEffects.GetCapabilities
---

# IWMPEffects::GetCapabilities


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCapabilities</b> method gets the capabilities of the visualization.

## -parameters

### -param pdwCapabilities [out]

<b>DWORD</b> containing the capabilities.

The current values are as follows.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>EFFECT_CANGOFULLSCREEN</b> = 0x00000001;</td>
<td>The visualization is capable of full-screen rendering.</td>
</tr>
<tr>
<td><b>EFFECT_HASPROPERTYPAGE</b> = 0x00000002;</td>
<td>The visualization has a property page.</td>
</tr>
<tr>
<td><b>EFFECT_VARIABLEFREQSTEP</b> = 0x00000004;</td>
<td>The visualization will use frequency data with variable size steps. If this bit is set, step size is based on the media sampling frequency divided by BUFFER_SIZE. If this bit is not set and media is played that was sampled at a low frequency, the upper cells will be empty. For example, if an 8KHz sampled file is played and this bit is not set, the upper half of the frequency array (from 8KHz to 22KHz) will be empty. If this bit is set and an 8Khz sampled file is played, the frequency array will range from 20Hz to 8KHz in BUFFER_SIZE steps.</td>
</tr>
<tr>
<td><b>EFFECT_WINDOWED_ONLY</b> = 0x00000008</td>
<td>The visualization only renders in windowed mode.</td>
</tr>
<tr>
<td><b>EFFECT2_FULLSCREENEXCLUSIVE</b> = 0x00000010</td>
<td>The visualization uses exclusive mode when rendering full-screen. The Player will not resize the window to fill the screen. The visualization must create a top level window and handle resolution switching.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

A default implementation of this method is not included in the visualization wizard.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>