---
UID: NF:wmp.IWMPPlayer2.put_windowlessVideo
title: IWMPPlayer2::put_windowlessVideo (wmp.h)
description: The put_windowlessVideo method specifies a value indicating whether the Windows Media Player control renders video in windowless mode.
helpviewer_keywords: ["IWMPPlayer2 interface [Windows Media Player]","put_windowlessVideo method","IWMPPlayer2.put_windowlessVideo","IWMPPlayer2::put_windowlessVideo","IWMPPlayer2put_windowlessVideo","put_windowlessVideo","put_windowlessVideo method [Windows Media Player]","put_windowlessVideo method [Windows Media Player]","IWMPPlayer2 interface","wmp.iwmpplayer2_put_windowlessvideo","wmp/IWMPPlayer2::put_windowlessVideo"]
old-location: wmp\iwmpplayer2_put_windowlessvideo.htm
tech.root: WMP
ms.assetid: 736eaf52-29bd-4223-a62d-d3d75cef1863
ms.date: 4/26/2023
ms.keywords: IWMPPlayer2 interface [Windows Media Player],put_windowlessVideo method, IWMPPlayer2.put_windowlessVideo, IWMPPlayer2::put_windowlessVideo, IWMPPlayer2put_windowlessVideo, put_windowlessVideo, put_windowlessVideo method [Windows Media Player], put_windowlessVideo method [Windows Media Player],IWMPPlayer2 interface, wmp.iwmpplayer2_put_windowlessvideo, wmp/IWMPPlayer2::put_windowlessVideo
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player for Windows XP or later.
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
 - IWMPPlayer2::put_windowlessVideo
 - wmp/IWMPPlayer2::put_windowlessVideo
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
 - IWMPPlayer2.put_windowlessVideo
---

# IWMPPlayer2::put_windowlessVideo


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_windowlessVideo</b> method specifies a value indicating whether the Windows Media Player control renders video in windowless mode.

## -parameters

### -param bEnabled [in]

<b>VARIANT_BOOL</b> indicating whether the Windows Media Player control renders video in windowless mode.

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

By default, an embedded Windows Media Player control renders video in its own window within the client area. When the <b>VARIANT_BOOL</b> specified in <b>put_windowlessVideo</b> is set to <b>TRUE</b>, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.

In Windows Vista, rendering video in windowless mode can degrade performance.

The <b>put_windowlessVideo</b> method is not supported for Netscape Navigator. Setting a value for this property in Navigator may yield unexpected results.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer2">IWMPPlayer2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayer2-get_windowlessvideo">IWMPPlayer2::get_windowlessVideo</a>