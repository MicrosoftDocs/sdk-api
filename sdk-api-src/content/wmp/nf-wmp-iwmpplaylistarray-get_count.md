---
UID: NF:wmp.IWMPPlaylistArray.get_count
title: IWMPPlaylistArray::get_count (wmp.h)
description: The get_count method retrieves the number of playlists in the playlist array.
helpviewer_keywords: ["IWMPPlaylistArray interface [Windows Media Player]","get_count method","IWMPPlaylistArray.get_count","IWMPPlaylistArray::get_count","IWMPPlaylistArrayget_count","get_count","get_count method [Windows Media Player]","get_count method [Windows Media Player]","IWMPPlaylistArray interface","wmp.iwmpplaylistarray_get_count","wmp/IWMPPlaylistArray::get_count"]
old-location: wmp\iwmpplaylistarray_get_count.htm
tech.root: WMP
ms.assetid: 2ce0058c-8839-43da-aad8-4bc423ff3cde
ms.date: 4/26/2023
ms.keywords: IWMPPlaylistArray interface [Windows Media Player],get_count method, IWMPPlaylistArray.get_count, IWMPPlaylistArray::get_count, IWMPPlaylistArrayget_count, get_count, get_count method [Windows Media Player], get_count method [Windows Media Player],IWMPPlaylistArray interface, wmp.iwmpplaylistarray_get_count, wmp/IWMPPlaylistArray::get_count
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
 - IWMPPlaylistArray::get_count
 - wmp/IWMPPlaylistArray::get_count
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
 - IWMPPlaylistArray.get_count
---

# IWMPPlaylistArray::get_count


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_count</b> method retrieves the number of playlists in the playlist array.

## -parameters

### -param plCount [out]

Pointer to a <b>long</b> containing the count.

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

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray">IWMPPlaylistArray Interface</a>