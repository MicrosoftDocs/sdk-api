---
UID: NF:wmp.IWMPSettings.get_autoStart
title: IWMPSettings::get_autoStart (wmp.h)
description: The get_autoStart method retrieves a value indicating whether the current media item begins playing automatically.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","get_autoStart method","IWMPSettings.get_autoStart","IWMPSettings::get_autoStart","IWMPSettingsget_autoStart","get_autoStart","get_autoStart method [Windows Media Player]","get_autoStart method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_get_autostart","wmp/IWMPSettings::get_autoStart"]
old-location: wmp\iwmpsettings_get_autostart.htm
tech.root: WMP
ms.assetid: 37180d0a-8fc4-4fe6-b190-97258803b43b
ms.date: 4/26/2023
ms.keywords: IWMPSettings interface [Windows Media Player],get_autoStart method, IWMPSettings.get_autoStart, IWMPSettings::get_autoStart, IWMPSettingsget_autoStart, get_autoStart, get_autoStart method [Windows Media Player], get_autoStart method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_get_autostart, wmp/IWMPSettings::get_autoStart
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
 - IWMPSettings::get_autoStart
 - wmp/IWMPSettings::get_autoStart
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
 - IWMPSettings.get_autoStart
---

# IWMPSettings::get_autoStart


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_autoStart</b> method retrieves a value indicating whether the current media item begins playing automatically.

## -parameters

### -param pfAutoStart [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates whether the current media item begins playing automatically. The default is <b>TRUE</b>.

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

If <i>pfAutoStart</i> is <b>TRUE</b>, the media item will begin playing when <b>IWMPCore::put_URL</b>, <b>IWMPCore::put_currentPlaylist</b>, or <b>IWMPCore::put_currentMedia</b> is called. Otherwise, the media item will not start playing until the <b>IWMPControls::play</b> method is called.

<i>pfAutoStart</i> for the full mode of Windows Media Player can be set globally by external events (such as loading a CD). Skins and remoted Player controls cannot expect a default value because they both employ the full mode Windows Media Player playback engine.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-play">IWMPControls::play</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">IWMPCore::put_URL</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentmedia">IWMPCore::put_currentMedia</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentplaylist">IWMPCore::put_currentPlaylist</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_autostart">IWMPSettings::put_autoStart</a>