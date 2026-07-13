---
UID: NF:wmp.IWMPSettings.get_volume
title: IWMPSettings::get_volume (wmp.h)
description: The get_volume method retrieves the current playback volume.
helpviewer_keywords: ["IWMPSetting2.get_volume","IWMPSetting2::get_volume","IWMPSettings interface [Windows Media Player]","get_volume method","IWMPSettings.get_volume","IWMPSettings::get_volume","IWMPSettingsget_volume","get_volume","get_volume method [Windows Media Player]","get_volume method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_volume","wmp/IWMPSettings::get_volume"]
old-location: wmp\iwmpsettings_get_volume.htm
tech.root: WMP
ms.assetid: 92c217e4-2ec4-4890-810c-dc552a36d578
ms.date: 4/26/2023
ms.keywords: IWMPSetting2.get_volume, IWMPSetting2::get_volume, IWMPSettings interface [Windows Media Player],get_volume method, IWMPSettings.get_volume, IWMPSettings::get_volume, IWMPSettingsget_volume, get_volume, get_volume method [Windows Media Player], get_volume method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_volume, wmp/IWMPSettings::get_volume
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
 - IWMPSettings::get_volume
 - wmp/IWMPSettings::get_volume
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
 - IWMPSettings.get_volume
 - IWMPSetting2::get_volume
 - IWMPSetting2.get_volume
---

# IWMPSettings::get_volume


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_volume</b> method retrieves the current playback volume.

## -parameters

### -param plVolume [out]

Pointer to a <b>long</b> containing the volume level ranging from 0 to 100.

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

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_volume">IWMPSetting::put_volume</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>