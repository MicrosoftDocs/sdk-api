---
UID: NF:wmp.IWMPSettings.put_volume
title: IWMPSettings::put_volume (wmp.h)
description: The put_volume method specifies the current playback volume.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","put_volume method","IWMPSettings.put_volume","IWMPSettings::put_volume","IWMPSettingsput_volume","put_volume","put_volume method [Windows Media Player]","put_volume method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_put_volume","wmp/IWMPSettings::put_volume"]
old-location: wmp\iwmpsettings_put_volume.htm
tech.root: WMP
ms.assetid: 435dac36-1ccf-41fd-94c2-1242c6af1bbd
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],put_volume method, IWMPSettings.put_volume, IWMPSettings::put_volume, IWMPSettingsput_volume, put_volume, put_volume method [Windows Media Player], put_volume method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_volume, wmp/IWMPSettings::put_volume
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
 - IWMPSettings::put_volume
 - wmp/IWMPSettings::put_volume
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
 - IWMPSettings.put_volume
---

# IWMPSettings::put_volume


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_volume</b> method specifies the current playback volume.

## -parameters

### -param lVolume [in]

<b>long</b> containing the volume level ranging from 0 to 100.

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

A value of zero specifies no volume (muted). A value of 100 specifies full volume. If no value is specified for this property, it defaults to the last volume setting established for Windows Media Player.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_volume">IWMPSettings::get_volume</a>