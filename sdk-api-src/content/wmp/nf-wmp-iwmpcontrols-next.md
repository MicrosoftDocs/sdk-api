---
UID: NF:wmp.IWMPControls.next
title: IWMPControls::next (wmp.h)
description: The next method sets the next item in the playlist as the current item.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","next method","IWMPControls.next","IWMPControls::next","IWMPControlsnext","next","next method [Windows Media Player]","next method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_next","wmp/IWMPControls::next"]
old-location: wmp\iwmpcontrols_next.htm
tech.root: WMP
ms.assetid: 1f0bbc77-b271-4076-8089-92fe7745d9a8
ms.date: 4/26/2023
ms.keywords: IWMPControls interface [Windows Media Player],next method, IWMPControls.next, IWMPControls::next, IWMPControlsnext, next, next method [Windows Media Player], next method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_next, wmp/IWMPControls::next
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
 - IWMPControls::next
 - wmp/IWMPControls::next
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
 - IWMPControls.next
---

# IWMPControls::next


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>next</b> method sets the next item in the playlist as the current item.



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

If the playlist is on the last entry when <b>next</b> is invoked, the first entry in the playlist will become the current one.

For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.

When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist. When playing DVD stills, this method skips to the next still.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-previous">IWMPControls::previous</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-stop">IWMPControls::stop</a>
