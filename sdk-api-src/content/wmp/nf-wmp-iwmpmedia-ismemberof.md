---
UID: NF:wmp.IWMPMedia.isMemberOf
title: IWMPMedia::isMemberOf (wmp.h)
description: The isMemberOf method retrieves a value indicating whether the specified media item is a member of the specified playlist.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","isMemberOf method","IWMPMedia.isMemberOf","IWMPMedia2 interface [Windows Media Player]","isMemberOf method","IWMPMedia2::isMemberOf","IWMPMedia3 interface [Windows Media Player]","isMemberOf method","IWMPMedia3::isMemberOf","IWMPMedia::isMemberOf","IWMPMediaisMemberOf","isMemberOf","isMemberOf method [Windows Media Player]","isMemberOf method [Windows Media Player]","IWMPMedia interface","isMemberOf method [Windows Media Player]","IWMPMedia2 interface","isMemberOf method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_ismemberof","wmp/IWMPMedia2::isMemberOf","wmp/IWMPMedia3::isMemberOf","wmp/IWMPMedia::isMemberOf"]
old-location: wmp\iwmpmedia_ismemberof.htm
tech.root: WMP
ms.assetid: 5ca46263-1e8e-42db-a131-e7534f79ca8e
ms.date: 4/26/2023
ms.keywords: IWMPMedia interface [Windows Media Player],isMemberOf method, IWMPMedia.isMemberOf, IWMPMedia2 interface [Windows Media Player],isMemberOf method, IWMPMedia2::isMemberOf, IWMPMedia3 interface [Windows Media Player],isMemberOf method, IWMPMedia3::isMemberOf, IWMPMedia::isMemberOf, IWMPMediaisMemberOf, isMemberOf, isMemberOf method [Windows Media Player], isMemberOf method [Windows Media Player],IWMPMedia interface, isMemberOf method [Windows Media Player],IWMPMedia2 interface, isMemberOf method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_ismemberof, wmp/IWMPMedia2::isMemberOf, wmp/IWMPMedia3::isMemberOf, wmp/IWMPMedia::isMemberOf
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
 - IWMPMedia::isMemberOf
 - wmp/IWMPMedia::isMemberOf
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
 - IWMPMedia.isMemberOf
 - IWMPMedia2.isMemberOf
 - IWMPMedia3.isMemberOf
---

# IWMPMedia::isMemberOf


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>isMemberOf</b> method retrieves a value indicating whether the specified media item is a member of the specified playlist.

## -parameters

### -param pPlaylist [in]

Pointer to an <b>IWMPPlaylist</b> interface.

### -param pvarfIsMemberOf [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates whether the item is a member of the playlist.

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

This method cannot check playlists retrieved through the <b>MediaCollection</b> object. To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the <b>IWMPCore::get_playlistCollection</b> method. Once you retrieve the collection, retrieve the individual playlist by calling the <b>IWMPPlaylistCollection::getByName</b> method.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_playlistcollection">IWMPCore::get_playlistCollection</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-getbyname">IWMPPlaylistCollection::getByName</a>