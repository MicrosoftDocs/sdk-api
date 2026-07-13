---
UID: NF:wmp.IWMPCore3.newPlaylist
title: IWMPCore3::newPlaylist (wmp.h)
description: The newPlaylist method retrieves a pointer to an IWMPPlaylist interface for a new playlist.
helpviewer_keywords: ["IWMPCore3 interface [Windows Media Player]","newPlaylist method","IWMPCore3.newPlaylist","IWMPCore3::newPlaylist","IWMPCore3newPlaylist","newPlaylist","newPlaylist method [Windows Media Player]","newPlaylist method [Windows Media Player]","IWMPCore3 interface","wmp.iwmpcore3_newplaylist","wmp/IWMPCore3::newPlaylist"]
old-location: wmp\iwmpcore3_newplaylist.htm
tech.root: WMP
ms.assetid: 61af7ce9-7fc6-4907-b423-3e6d2d8f39ac
ms.date: 4/26/2023
ms.keywords: IWMPCore3 interface [Windows Media Player],newPlaylist method, IWMPCore3.newPlaylist, IWMPCore3::newPlaylist, IWMPCore3newPlaylist, newPlaylist, newPlaylist method [Windows Media Player], newPlaylist method [Windows Media Player],IWMPCore3 interface, wmp.iwmpcore3_newplaylist, wmp/IWMPCore3::newPlaylist
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
 - IWMPCore3::newPlaylist
 - wmp/IWMPCore3::newPlaylist
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
 - IWMPCore3.newPlaylist
---

# IWMPCore3::newPlaylist


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>newPlaylist</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface for a new playlist.

## -parameters

### -param bstrName [in]

<b>BSTR</b> containing the playlist name.

### -param bstrURL [in]

<b>BSTR</b> containing the playlist URL.

### -param ppPlaylist [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface.

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

If the <i>bstrURL</i> parameter is a null or empty string, this method creates an empty <b>Playlist</b> object. If the <i>bstrname</i> parameter is an empty string, this method applies the current metafile name.

The new playlist created with this method is not added to the library. To add a new playlist to the library, use <b>IWMPPlaylistCollection::importPlaylist</b> or <b>IWMPPlaylistCollection::newPlaylist</b>. Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.

Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore3">IWMPCore3 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-importplaylist">IWMPPlaylistCollection::importPlaylist</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist">IWMPPlaylistCollection::newPlaylist</a>