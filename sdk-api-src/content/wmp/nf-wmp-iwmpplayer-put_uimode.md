---
UID: NF:wmp.IWMPPlayer.put_uiMode
title: IWMPPlayer::put_uiMode (wmp.h)
description: The put_uiMode method specifies a value indicating which controls are shown in the user interface.
helpviewer_keywords: ["IWMPPlayer interface [Windows Media Player]","put_uiMode method","IWMPPlayer.put_uiMode","IWMPPlayer::put_uiMode","IWMPPlayerput_uiMode","put_uiMode","put_uiMode method [Windows Media Player]","put_uiMode method [Windows Media Player]","IWMPPlayer interface","wmp.iwmpplayer_put_uimode","wmp/IWMPPlayer::put_uiMode"]
old-location: wmp\iwmpplayer_put_uimode.htm
tech.root: WMP
ms.assetid: 154db914-a0c3-44de-b692-e1b7f9c681f6
ms.date: 4/26/2023
ms.keywords: IWMPPlayer interface [Windows Media Player],put_uiMode method, IWMPPlayer.put_uiMode, IWMPPlayer::put_uiMode, IWMPPlayerput_uiMode, put_uiMode, put_uiMode method [Windows Media Player], put_uiMode method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_put_uimode, wmp/IWMPPlayer::put_uiMode
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
 - IWMPPlayer::put_uiMode
 - wmp/IWMPPlayer::put_uiMode
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
 - IWMPPlayer.put_uiMode
---

# IWMPPlayer::put_uiMode


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_uiMode</b> method specifies a value indicating which controls are shown in the user interface.

## -parameters

### -param bstrMode [in]

<b>BSTR</b> containing one of the following values.

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

This method specifies the appearance of the embedded Windows Media Player. When the <b>BSTR</b> specified in <b>put_uiMode</b> is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations. This window can be hidden in mini or full mode by setting the <b>height</b> attribute of the <b>OBJECT</b> tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible. If no embedded interface is desired, set both the <b>width</b> and <b>height</b> attributes to zero.

If the <b>BSTR</b> specified in <b>put_uiMode</b> is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by <b>width</b> and <b>height</b>. This is useful for retaining page layout whenever the UI mode changes. Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.

If the <b>BSTR</b> specified in <b>put_uiMode</b> is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode. If the <b>BSTR</b> specified in <b>put_uiMode</b> is set to "none", no controls are displayed in full-screen mode.

If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.

If the <b>BSTR</b> specified in <b>put_uiMode</b> is set to "custom" in a C++ program that implements <b>IWMPRemoteMediaServices</b>, the skin file indicated by <b>IWMPRemoteMediaServices::GetCustomUIMode</b> is displayed.

During full-screen playback, Windows Media Player hides the mouse cursor when the <b>VARIANT_BOOL</b> retrieved from <b>IWMPPlayer::get_enableContextMenu</b> equals <b>FALSE</b> and the <b>BSTR</b> retrieved from <b>IWMPPlayer::get_uiMode</b> equals "none".

<b>Windows Media Player 10 Mobile: </b>This method only specifies a <b>BSTR</b> set to "none" or "full". On Smartphone devices, only playback status and a counter are displayed when setting <b>uiMode</b> to "full".

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_enablecontextmenu">IWMPPlayer::get_enableContextMenu</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_uimode">IWMPPlayer::get_uiMode</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices">IWMPRemoteMediaServices Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode">IWMPRemoteMediaServices::GetCustomUIMode</a>