---
UID: NF:wmp.IWMPControls.stop
title: IWMPControls::stop (wmp.h)
description: The stop method stops playback of the media item.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","stop method","IWMPControls.stop","IWMPControls::stop","IWMPControlsstop","stop","stop method [Windows Media Player]","stop method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_stop","wmp/IWMPControls::stop"]
old-location: wmp\iwmpcontrols_stop.htm
tech.root: WMP
ms.assetid: 97ab009d-5ad9-4049-a212-1ef95941f951
ms.date: 4/26/2023
ms.keywords: IWMPControls interface [Windows Media Player],stop method, IWMPControls.stop, IWMPControls::stop, IWMPControlsstop, stop, stop method [Windows Media Player], stop method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_stop, wmp/IWMPControls::stop
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
 - IWMPControls::stop
 - wmp/IWMPControls::stop
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
 - IWMPControls.stop
---

# IWMPControls::stop


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>stop</b> method stops playback of the media item.



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

This method causes Windows Media Player to release any system resources it is using, such as the audio device. The current media item, however, is not released.

When Windows Media Player is stopped, the current playback point in the media item is reset to the beginning of the item. Subsequently calling <b>IWMPControls::play</b> will start playback from the beginning of the media item. To halt a play operation without changing the current position, use the <b>IWMPControls::pause</b> method.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-next">IWMPControls::next</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-pause">IWMPControls::pause</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-play">IWMPControls::play</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-previous">IWMPControls::previous</a>
