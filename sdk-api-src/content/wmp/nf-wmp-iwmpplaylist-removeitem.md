---
UID: NF:wmp.IWMPPlaylist.removeItem
title: IWMPPlaylist::removeItem (wmp.h)
description: The removeItem method removes the specified media item from the playlist.
helpviewer_keywords: ["IWMPPlaylist interface [Windows Media Player]","removeItem method","IWMPPlaylist.removeItem","IWMPPlaylist::removeItem","IWMPPlaylistremoveItem","removeItem","removeItem method [Windows Media Player]","removeItem method [Windows Media Player]","IWMPPlaylist interface","wmp.iwmpplaylist_removeitem","wmp/IWMPPlaylist::removeItem"]
old-location: wmp\iwmpplaylist_removeitem.htm
tech.root: WMP
ms.assetid: 7a17b0e0-2eaf-4570-a297-c2540ae4b6c5
ms.date: 4/26/2023
ms.keywords: IWMPPlaylist interface [Windows Media Player],removeItem method, IWMPPlaylist.removeItem, IWMPPlaylist::removeItem, IWMPPlaylistremoveItem, removeItem, removeItem method [Windows Media Player], removeItem method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_removeitem, wmp/IWMPPlaylist::removeItem
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
 - IWMPPlaylist::removeItem
 - wmp/IWMPPlaylist::removeItem
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
 - IWMPPlaylist.removeItem
---

# IWMPPlaylist::removeItem


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>removeItem</b> method removes the specified media item from the playlist.

## -parameters

### -param pIWMPMedia [in]

Pointer to an <b>IWMPMedia</b> interface for the item to remove.

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

If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.

If there is no next item, the previous item is used. If there are no other items, then the <b>IWMPCore::get_currentMedia</b> method will return <b>NULL</b>.

Before calling this method, you must have full access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_currentmedia">IWMPCore::get_currentMedia</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-insertitem">IWMPPlaylist::insertItem</a>