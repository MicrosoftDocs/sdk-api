---
UID: NF:wmp.IWMPCdromBurn.put_burnPlaylist
title: IWMPCdromBurn::put_burnPlaylist (wmp.h)
description: The put_burnPlaylist method specifies the playlist to burn to CD.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","put_burnPlaylist method","IWMPCdromBurn.put_burnPlaylist","IWMPCdromBurn::put_burnPlaylist","IWMPCdromBurnput_burnPlaylist","put_burnPlaylist","put_burnPlaylist method [Windows Media Player]","put_burnPlaylist method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_put_burnplaylist","wmp/IWMPCdromBurn::put_burnPlaylist"]
old-location: wmp\iwmpcdromburn_put_burnplaylist.htm
tech.root: WMP
ms.assetid: 26fad65c-d371-4e7c-a86e-1ddb24175909
ms.date: 4/26/2023
ms.keywords: IWMPCdromBurn interface [Windows Media Player],put_burnPlaylist method, IWMPCdromBurn.put_burnPlaylist, IWMPCdromBurn::put_burnPlaylist, IWMPCdromBurnput_burnPlaylist, put_burnPlaylist, put_burnPlaylist method [Windows Media Player], put_burnPlaylist method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_put_burnplaylist, wmp/IWMPCdromBurn::put_burnPlaylist
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromBurn::put_burnPlaylist
 - wmp/IWMPCdromBurn::put_burnPlaylist
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
 - IWMPCdromBurn.put_burnPlaylist
---

# IWMPCdromBurn::put_burnPlaylist


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_burnPlaylist</b> method specifies the playlist to burn to CD.

## -parameters

### -param pPlaylist [in]

Pointer to an <b>IWMPPlaylist</b> interface for the playlist to burn.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnplaylist">IWMPCdromBurn::get_burnPlaylist</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>