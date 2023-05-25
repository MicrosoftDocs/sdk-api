---
UID: NF:wmp.IWMPPlaylistCollection.newPlaylist
title: IWMPPlaylistCollection::newPlaylist (wmp.h)
description: The newPlaylist method creates a new, empty playlist in the library.
helpviewer_keywords: ["IWMPPlaylistCollection interface [Windows Media Player]","newPlaylist method","IWMPPlaylistCollection.newPlaylist","IWMPPlaylistCollection::newPlaylist","IWMPPlaylistCollectionnewPlaylist","newPlaylist","newPlaylist method [Windows Media Player]","newPlaylist method [Windows Media Player]","IWMPPlaylistCollection interface","wmp.iwmpplaylistcollection_newplaylist","wmp/IWMPPlaylistCollection::newPlaylist"]
old-location: wmp\iwmpplaylistcollection_newplaylist.htm
tech.root: WMP
ms.assetid: 5ad51469-a150-4322-ac16-782ef0d96a57
ms.date: 4/26/2023
ms.keywords: IWMPPlaylistCollection interface [Windows Media Player],newPlaylist method, IWMPPlaylistCollection.newPlaylist, IWMPPlaylistCollection::newPlaylist, IWMPPlaylistCollectionnewPlaylist, newPlaylist, newPlaylist method [Windows Media Player], newPlaylist method [Windows Media Player],IWMPPlaylistCollection interface, wmp.iwmpplaylistcollection_newplaylist, wmp/IWMPPlaylistCollection::newPlaylist
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
 - IWMPPlaylistCollection::newPlaylist
 - wmp/IWMPPlaylistCollection::newPlaylist
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
 - IWMPPlaylistCollection.newPlaylist
---

# IWMPPlaylistCollection::newPlaylist


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>newPlaylist</b> method creates a new, empty playlist in the library.

## -parameters

### -param bstrName [in]

String containing the name of the new playlist.

### -param ppItem [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the new playlist.

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

This method creates an empty playlist in the library. To fill the playlist with media items, use <b>IWMPPlaylist::appendItem</b> or <b>IWMPPlaylist::insertItem</b>.

Multiple playlists having the same name are permitted in the library. To avoid creating a duplicate playlist name with this method, use the <b>getByName</b> method and <b>IWMPPlaylistArray::count</b> to determine whether a playlist with a particular name already exists.

Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the bstrName parameter.

Before calling this method, you must have full access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-appenditem">IWMPPlaylist::appendItem</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-insertitem">IWMPPlaylist::insertItem</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-get_count">IWMPPlaylistArray::get_count</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection">IWMPPlaylistCollection Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-getbyname">IWMPPlaylistCollection::getByName</a>