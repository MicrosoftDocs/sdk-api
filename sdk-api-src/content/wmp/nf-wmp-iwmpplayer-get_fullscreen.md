---
UID: NF:wmp.IWMPPlayer.get_fullScreen
title: IWMPPlayer::get_fullScreen (wmp.h)
description: The get_fullScreen method retrieves a value indicating whether video content is played back in full-screen mode.
helpviewer_keywords: ["IWMPPlayer interface [Windows Media Player]","get_fullScreen method","IWMPPlayer.get_fullScreen","IWMPPlayer::get_fullScreen","IWMPPlayerget_fullScreen","get_fullScreen","get_fullScreen method [Windows Media Player]","get_fullScreen method [Windows Media Player]","IWMPPlayer interface","wmp.iwmpplayer_get_fullscreen","wmp/IWMPPlayer::get_fullScreen"]
old-location: wmp\iwmpplayer_get_fullscreen.htm
tech.root: WMP
ms.assetid: 5a8bb0b5-76c6-424f-ba37-5e913b6ed542
ms.date: 4/26/2023
ms.keywords: IWMPPlayer interface [Windows Media Player],get_fullScreen method, IWMPPlayer.get_fullScreen, IWMPPlayer::get_fullScreen, IWMPPlayerget_fullScreen, get_fullScreen, get_fullScreen method [Windows Media Player], get_fullScreen method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_get_fullscreen, wmp/IWMPPlayer::get_fullScreen
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
 - IWMPPlayer::get_fullScreen
 - wmp/IWMPPlayer::get_fullScreen
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
 - IWMPPlayer.get_fullScreen
---

# IWMPPlayer::get_fullScreen


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_fullScreen</b> method retrieves a value indicating whether video content is played back in full-screen mode.

## -parameters

### -param pbFullScreen [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether video content is played back in full-screen mode. The default is <b>FALSE</b>.

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

For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel. If the <b>BSTR</b> specified in <b>IWMPPlayer::put_uiMode</b> is set to "mini" or "full", the height of the control itself must be 65 pixels or greater to accommodate the video display area in addition to the user interface.

If the <b>BSTR</b> specified in <b>IWMPPlayer::put_uiMode</b> is set to "invisible", then specifying the <b>VARIANT_BOOL</b> to <b>TRUE</b> in <b>get_fullScreen</b> raises an error and does not affect the behavior of the control.

During full-screen playback, Windows Media Player hides the mouse cursor when the <b>VARIANT_BOOL</b> retrieved from <b>IWMPPlayer::get_enableContextMenu</b> equals <b>FALSE</b> and the <b>BSTR</b> retrieved from <b>IWMPPlayer::get_uiMode</b> equals "none".

If the <b>BSTR</b> specified in <b>IWMPPlayer::put_uiMode</b> is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves. After a brief interval of no mouse movement, the transport controls are hidden. If the <b>BSTR</b> specified in <b>IWMPPlayer::put_uiMode</b> is set to "none", no controls are displayed in full-screen mode.

Note
        

Displaying transport controls in full-screen mode requires the Windows XP operating system.

If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_enablecontextmenu">IWMPPlayer::get_enableContextMenu</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_fullscreen">IWMPPlayer::put_fullScreen</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_uimode">IWMPPlayer::put_uiMode</a>