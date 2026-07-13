---
UID: NF:wmp.IWMPPlayer.put_enabled
title: IWMPPlayer::put_enabled (wmp.h)
description: The put_enabled method specifies a value indicating whether the Windows Media Player control is enabled.
helpviewer_keywords: ["IWMPPlayer interface [Windows Media Player]","put_enabled method","IWMPPlayer.put_enabled","IWMPPlayer::put_enabled","IWMPPlayerput_enabled","put_enabled","put_enabled method [Windows Media Player]","put_enabled method [Windows Media Player]","IWMPPlayer interface","wmp.iwmpplayer_put_enabled","wmp/IWMPPlayer::put_enabled"]
old-location: wmp\iwmpplayer_put_enabled.htm
tech.root: WMP
ms.assetid: c0e29724-1689-4b59-a9bd-b9cc3f391b68
ms.date: 4/26/2023
ms.keywords: IWMPPlayer interface [Windows Media Player],put_enabled method, IWMPPlayer.put_enabled, IWMPPlayer::put_enabled, IWMPPlayerput_enabled, put_enabled, put_enabled method [Windows Media Player], put_enabled method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_put_enabled, wmp/IWMPPlayer::put_enabled
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
 - IWMPPlayer::put_enabled
 - wmp/IWMPPlayer::put_enabled
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
 - IWMPPlayer.put_enabled
---

# IWMPPlayer::put_enabled


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_enabled</b> method specifies a value indicating whether the Windows Media Player control is enabled.

## -parameters

### -param bEnabled [in]

<b>VARIANT_BOOL</b> indicating whether the Windows Media Player control is enabled.

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

If the <b>VARIANT_BOOL</b> specified in <b>put_enabled</b> is set to <b>FALSE</b>, then Windows Media Player hides the user controls during full-screen playback.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-get_enabled">IWMPPlayer::get_enabled</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer-put_enablecontextmenu">IWMPPlayer::put_enableContextMenu</a>