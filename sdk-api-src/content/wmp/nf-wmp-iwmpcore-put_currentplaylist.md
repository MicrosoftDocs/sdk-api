---
UID: NF:wmp.IWMPCore.put_currentPlaylist
title: IWMPCore::put_currentPlaylist (wmp.h)
description: The put_currentPlaylist method specifies the IWMPPlaylist interface that corresponds to the current playlist.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","put_currentPlaylist method","IWMPCore.put_currentPlaylist","IWMPCore::put_currentPlaylist","IWMPCoreput_currentPlaylist","put_currentPlaylist","put_currentPlaylist method [Windows Media Player]","put_currentPlaylist method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_put_currentplaylist","wmp/IWMPCore::put_currentPlaylist"]
old-location: wmp\iwmpcore_put_currentplaylist.htm
tech.root: WMP
ms.assetid: 943641ca-9733-4066-bc69-834e792d93dc
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],put_currentPlaylist method, IWMPCore.put_currentPlaylist, IWMPCore::put_currentPlaylist, IWMPCoreput_currentPlaylist, put_currentPlaylist, put_currentPlaylist method [Windows Media Player], put_currentPlaylist method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_put_currentplaylist, wmp/IWMPCore::put_currentPlaylist
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
 - IWMPCore::put_currentPlaylist
 - wmp/IWMPCore::put_currentPlaylist
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
 - IWMPCore.put_currentPlaylist
---

# IWMPCore::put_currentPlaylist


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_currentPlaylist</b> method specifies the <b>IWMPPlaylist</b> interface that corresponds to the current playlist.

## -parameters

### -param pPL [in]

Pointer to an <b>IWMPPlaylist</b> interface.

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

If the <b>IWMPSettings::put_autoStart</b> method was invoked with an argument of true, file playback will begin automatically whenever you invoke <b>put_currentPlaylist</b>.

You can retrieve an <b>IWMPMedia</b> interface for a given media object by invoking the <b>IWMPPlaylist::get_Item</b> method.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_currentplaylist">IWMPCore::get_currentPlaylist</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>