---
UID: NF:wmp.IWMPSettings.setMode
title: IWMPSettings::setMode (wmp.h)
description: The setMode method sets the state of playback options.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","setMode method","IWMPSettings.setMode","IWMPSettings::setMode","IWMPSettingssetMode","setMode","setMode method [Windows Media Player]","setMode method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_setmode","wmp/IWMPSettings::setMode"]
old-location: wmp\iwmpsettings_setmode.htm
tech.root: WMP
ms.assetid: 28a404a7-5bb0-41bb-a5b2-cc6138b8176e
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],setMode method, IWMPSettings.setMode, IWMPSettings::setMode, IWMPSettingssetMode, setMode, setMode method [Windows Media Player], setMode method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_setmode, wmp/IWMPSettings::setMode
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSettings::setMode
 - wmp/IWMPSettings::setMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSettings.setMode
---

# IWMPSettings::setMode


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>setMode</b> method sets the state of playback options.

## -parameters

### -param bstrMode [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>autoRewind</td>
<td>Tracks are restarted at the beginning after playing to the end. Default state is true.</td>
</tr>
<tr>
<td>loop</td>
<td>The sequence of tracks repeats itself. Default state is false.</td>
</tr>
<tr>
<td>showFrame</td>
<td>The nearest video keyframe is displayed when not playing. Default state is false. Has no effect on audio tracks.</td>
</tr>
<tr>
<td>shuffle</td>
<td>Tracks are played in random order. Default state is false.</td>
</tr>
</table>

### -param varfMode [in]

<b>VARIANT_BOOL</b> specifying whether the specified mode is active.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame. Use this mode cautiously when playing non-local content.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-getmode">IWMPSettings::getMode</a>