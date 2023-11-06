---
UID: NF:wmp.IWMPPlaylist.appendItem
title: IWMPPlaylist::appendItem (wmp.h)
description: The appendItem method adds a media item to the end of the playlist.
helpviewer_keywords: ["IWMPPlaylist interface [Windows Media Player]","appendItem method","IWMPPlaylist.appendItem","IWMPPlaylist::appendItem","IWMPPlaylistappendItem","appendItem","appendItem method [Windows Media Player]","appendItem method [Windows Media Player]","IWMPPlaylist interface","wmp.iwmpplaylist_appenditem","wmp/IWMPPlaylist::appendItem"]
old-location: wmp\iwmpplaylist_appenditem.htm
tech.root: WMP
ms.assetid: e6db41d8-a4d5-4cab-9612-0562f3e92c25
ms.date: 4/26/2023
ms.keywords: IWMPPlaylist interface [Windows Media Player],appendItem method, IWMPPlaylist.appendItem, IWMPPlaylist::appendItem, IWMPPlaylistappendItem, appendItem, appendItem method [Windows Media Player], appendItem method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_appenditem, wmp/IWMPPlaylist::appendItem
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
 - IWMPPlaylist::appendItem
 - wmp/IWMPPlaylist::appendItem
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
 - IWMPPlaylist.appendItem
---

# IWMPPlaylist::appendItem


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>appendItem</b> method adds a media item to the end of the playlist.

## -parameters

### -param pIWMPMedia [in]

Pointer to an <b>IWMPMedia</b> interface.

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

Before calling this method, you must have full access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>