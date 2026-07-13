---
UID: NF:wmp.IWMPPlaylist.get_name
title: IWMPPlaylist::get_name (wmp.h)
description: The get_name method retrieves the name of the playlist.
helpviewer_keywords: ["IWMPPlaylist interface [Windows Media Player]","get_name method","IWMPPlaylist.get_name","IWMPPlaylist::get_name","IWMPPlaylistget_name","get_name","get_name method [Windows Media Player]","get_name method [Windows Media Player]","IWMPPlaylist interface","wmp.iwmpplaylist_get_name","wmp/IWMPPlaylist::get_name"]
old-location: wmp\iwmpplaylist_get_name.htm
tech.root: WMP
ms.assetid: 547a8ebe-b7c7-4dbc-96c4-1d5f5ef77f97
ms.date: 4/26/2023
ms.keywords: IWMPPlaylist interface [Windows Media Player],get_name method, IWMPPlaylist.get_name, IWMPPlaylist::get_name, IWMPPlaylistget_name, get_name, get_name method [Windows Media Player], get_name method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_get_name, wmp/IWMPPlaylist::get_name
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
 - IWMPPlaylist::get_name
 - wmp/IWMPPlaylist::get_name
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
 - IWMPPlaylist.get_name
---

# IWMPPlaylist::get_name


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_name</b> method retrieves the name of the playlist.

## -parameters

### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-put_name">IWMPPlaylist::put_name</a>