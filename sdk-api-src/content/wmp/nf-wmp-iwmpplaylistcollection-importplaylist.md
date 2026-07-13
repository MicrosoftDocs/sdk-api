---
UID: NF:wmp.IWMPPlaylistCollection.importPlaylist
title: IWMPPlaylistCollection::importPlaylist (wmp.h)
description: The importPlaylist method adds a static playlist to the library.
helpviewer_keywords: ["IWMPPlaylistCollection interface [Windows Media Player]","importPlaylist method","IWMPPlaylistCollection.importPlaylist","IWMPPlaylistCollection::importPlaylist","IWMPPlaylistCollectionimportPlaylist","importPlaylist","importPlaylist method [Windows Media Player]","importPlaylist method [Windows Media Player]","IWMPPlaylistCollection interface","wmp.iwmpplaylistcollection_importplaylist","wmp/IWMPPlaylistCollection::importPlaylist"]
old-location: wmp\iwmpplaylistcollection_importplaylist.htm
tech.root: WMP
ms.assetid: 421a1bd3-65c1-4d8f-be75-918b1cfa06d2
ms.date: 4/26/2023
ms.keywords: IWMPPlaylistCollection interface [Windows Media Player],importPlaylist method, IWMPPlaylistCollection.importPlaylist, IWMPPlaylistCollection::importPlaylist, IWMPPlaylistCollectionimportPlaylist, importPlaylist, importPlaylist method [Windows Media Player], importPlaylist method [Windows Media Player],IWMPPlaylistCollection interface, wmp.iwmpplaylistcollection_importplaylist, wmp/IWMPPlaylistCollection::importPlaylist
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
 - IWMPPlaylistCollection::importPlaylist
 - wmp/IWMPPlaylistCollection::importPlaylist
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
 - IWMPPlaylistCollection.importPlaylist
---

# IWMPPlaylistCollection::importPlaylist


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>importPlaylist</b> method adds a static playlist to the library.

## -parameters

### -param pItem [in]

Pointer to an <b>IWMPPlaylist</b> interface for the playlist that this method will add.

### -param ppImportedItem [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the added playlist.

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

Playlists that do not contain any media items cannot be added to the library by using this method. To create an empty playlist in the library, use the <b>newPlaylist</b> method. You can then fill the resulting playlist with media items by using <b>IWMPPlaylist::appendItem</b> or <b>IWMPPlaylist::insertItem</b>.

If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist. To add an auto playlist to the library and preserve its automatic behavior, use <b>IWMPMediaCollection::add</b>. For more information, see <a href="/windows/desktop/WMP/static-and-auto-playlists">Static and Auto Playlists</a>.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-appenditem">IWMPPlaylist::appendItem</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-insertitem">IWMPPlaylist::insertItem</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection">IWMPPlaylistCollection Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist">IWMPPlaylistCollection::newPlaylist</a>