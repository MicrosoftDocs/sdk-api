---
UID: NF:wmp.IWMPPlayer.get_uiMode
title: IWMPPlayer::get_uiMode (wmp.h)
description: The get_uiMode method retrieves a value indicating which controls are shown in the user interface.
helpviewer_keywords: ["IWMPPlayer interface [Windows Media Player]","get_uiMode method","IWMPPlayer.get_uiMode","IWMPPlayer::get_uiMode","IWMPPlayerget_uiMode","get_uiMode","get_uiMode method [Windows Media Player]","get_uiMode method [Windows Media Player]","IWMPPlayer interface","wmp.iwmpplayer_get_uimode","wmp/IWMPPlayer::get_uiMode"]
old-location: wmp\iwmpplayer_get_uimode.htm
tech.root: WMP
ms.assetid: 8e05342f-812a-4dca-a491-b237f9a9f1bd
ms.date: 4/26/2023
ms.keywords: IWMPPlayer interface [Windows Media Player],get_uiMode method, IWMPPlayer.get_uiMode, IWMPPlayer::get_uiMode, IWMPPlayerget_uiMode, get_uiMode, get_uiMode method [Windows Media Player], get_uiMode method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_get_uimode, wmp/IWMPPlayer::get_uiMode
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
 - IWMPPlayer::get_uiMode
 - wmp/IWMPPlayer::get_uiMode
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
 - IWMPPlayer.get_uiMode
---

# IWMPPlayer::get_uiMode


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_uiMode</b> method retrieves a value indicating which controls are shown in the user interface.

## -parameters

### -param pbstrMode [out]

Pointer to a <b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
<th>Audio example
                </th>
<th>Video example
                </th>
</tr>
<tr>
<td>invisible</td>
<td>Windows Media Player is embedded without any visible user interface (controls, video, or visualization window).</td>
<td>(Nothing is displayed.)</td>
<td>(Nothing is displayed.)</td>
</tr>
<tr>
<td>none</td>
<td>Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</td>
<td><img alt='uiMode="none" with audio' border="0" src="./images/uimode_none_audio_v11.png"/></td>
<td><img alt='uiMode="none" with video' border="0" src="./images/uimode_none_video_v11.png"/></td>
</tr>
<tr>
<td>mini</td>
<td>Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</td>
<td><img alt='uiMode="mini" with audio' border="0" src="./images/uimode_mini_audio_v11.png"/></td>
<td><img alt='uiMode="mini" with video' border="0" src="./images/uimode_mini_video_v11.png"/></td>
</tr>
<tr>
<td>full</td>
<td>Default. Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, fast reverse, and volume controls in addition to the video or visualization window.</td>
<td><img alt='uiMode="full" with audio' border="0" src="./images/uimode_full_audio_v11.png"/></td>
<td><img alt='uiMode="full" with video' border="0" src="./images/uimode_full_video_v11.png"/></td>
</tr>
<tr>
<td>custom</td>
<td>Windows Media Player is embedded with a custom user interface. Can only be used in C++ programs.</td>
<td>(Custom user interface is displayed.)</td>
<td>(Custom user interface is displayed.)</td>
</tr>
</table>

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

This method retrieves the appearance of the embedded Windows Media Player. When the <b>BSTR</b> retrieved from <b>get_uiMode</b> is "none", "mini", or "full", a window is present for the display of video clips and audio visualizations. This window can be hidden in mini or full mode by setting the <b>height</b> attribute of the <b>OBJECT</b> tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible. If no embedded interface is desired, set both the <b>width</b> and <b>height</b> attributes to zero.

If the <b>BSTR</b> retrieved from <b>get_uiMode</b> is "invisible", no user interface is displayed, but space is still reserved on the page as specified by <b>width</b> and <b>height</b>. This is useful for retaining page layout whenever the UI mode changes. Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.

If the <b>BSTR</b> retrieved from <b>get_uiMode</b> is "full" or "mini", Windows Media Player displays transport controls in full-screen mode. If the <b>BSTR</b> retrieved from <b>get_uiMode</b> is "none", no controls are displayed in full-screen mode.

If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.

If the <b>BSTR</b> retrieved from <b>get_uiMode</b> is "custom" in a C++ program that implements <b>IWMPRemoteMediaServices</b>, the skin file indicated by <b>IWMPRemoteMediaServices::GetCustomUIMode</b> is displayed.

During full-screen playback, Windows Media Player hides the mouse cursor when the <b>VARIANT_BOOL</b> received from <b>IWMPPlayer::get_enableContextMenu</b> equals <b>FALSE</b> and the <b>BSTR</b> received from <b>get_uiMode</b> equals "none".

<b>Windows Media Player 10 Mobile: </b>This method only retrieves a <b>BSTR</b> set to "none" or "full". On Smartphone devices, only playback status and a counter are displayed when <b>uiMode</b> is set to "full".

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_enablecontextmenu">IWMPPlayer::get_enableContextMenu</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_uimode">IWMPPlayer::put_uiMode</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices">IWMPRemoteMediaServices Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode">IWMPRemoteMediaServices::GetCustomUIMode</a>