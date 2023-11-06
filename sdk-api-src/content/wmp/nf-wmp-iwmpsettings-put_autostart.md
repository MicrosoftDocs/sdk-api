---
UID: NF:wmp.IWMPSettings.put_autoStart
title: IWMPSettings::put_autoStart (wmp.h)
description: The put_autoStart method specifies a value indicating whether the current media item begins playing automatically.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","put_autoStart method","IWMPSettings.put_autoStart","IWMPSettings::put_autoStart","IWMPSettingsput_autoStart","put_autoStart","put_autoStart method [Windows Media Player]","put_autoStart method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_put_autostart","wmp/IWMPSettings::put_autoStart"]
old-location: wmp\iwmpsettings_put_autostart.htm
tech.root: WMP
ms.assetid: 34f80fa4-6e9c-4435-b360-55c2856f89fb
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],put_autoStart method, IWMPSettings.put_autoStart, IWMPSettings::put_autoStart, IWMPSettingsput_autoStart, put_autoStart, put_autoStart method [Windows Media Player], put_autoStart method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_autostart, wmp/IWMPSettings::put_autoStart
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
 - IWMPSettings::put_autoStart
 - wmp/IWMPSettings::put_autoStart
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
 - IWMPSettings.put_autoStart
---

# IWMPSettings::put_autoStart


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_autoStart</b> method specifies a value indicating whether the current media item begins playing automatically.

## -parameters

### -param fAutoStart [in]

<b>VARIANT_BOOL</b> indicating whether the current media item begins playing automatically. The default is <b>TRUE</b>.

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

The <b>put_autoStart</b> method for the full mode of Windows Media Player can be set globally by external events (such as loading a CD). Therefore, there is no reliable default value for skins and remoted Player controls. This is because the playback engine of the full mode Player is used in both cases.

You should set <b>put_autoStart</b> to <b>FALSE</b> immediately before you set <b>IWMPCore::put_URL</b>, <b>IWMPCore::put_currentPlaylist</b>, or <b>IWMPCore::put_currentMedia</b> in skins and remoted Player controls if you wish to ensure that the media item does not start playing immediately. Also, unless you set <b>put_autostart</b> to <b>TRUE</b> immediately before specifying a media item, you should not rely on this setting as a substitute for using the <b>IWMPControls::play</b> method.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-play">IWMPControls::play</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentmedia">IWMPCore::put_currentMedia</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentplaylist">IWMPCore::put_currentPlaylist</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_autostart">IWMPSettings::get_autoStart</a>