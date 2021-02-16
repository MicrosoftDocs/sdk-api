---
UID: NF:wmp.IWMPPlaylist.get_attributeCount
title: IWMPPlaylist::get_attributeCount (wmp.h)
description: The get_attributeCount method retrieves the number of attributes associated with the playlist.
helpviewer_keywords: ["IWMPPlaylist interface [Windows Media Player]","get_attributeCount method","IWMPPlaylist.get_attributeCount","IWMPPlaylist::get_attributeCount","IWMPPlaylistget_attributeCount","get_attributeCount","get_attributeCount method [Windows Media Player]","get_attributeCount method [Windows Media Player]","IWMPPlaylist interface","wmp.iwmpplaylist_get_attributecount","wmp/IWMPPlaylist::get_attributeCount"]
old-location: wmp\iwmpplaylist_get_attributecount.htm
tech.root: WMP
ms.assetid: 32c18feb-4df2-41d6-9adf-49836b6b836d
ms.date: 12/05/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],get_attributeCount method, IWMPPlaylist.get_attributeCount, IWMPPlaylist::get_attributeCount, IWMPPlaylistget_attributeCount, get_attributeCount, get_attributeCount method [Windows Media Player], get_attributeCount method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_get_attributecount, wmp/IWMPPlaylist::get_attributeCount
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
 - IWMPPlaylist::get_attributeCount
 - wmp/IWMPPlaylist::get_attributeCount
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
 - IWMPPlaylist.get_attributeCount
---

# IWMPPlaylist::get_attributeCount


## -description

The <b>get_attributeCount</b> method retrieves the number of attributes associated with the playlist.

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

Because playlists can come from many different sources, they can have several different sets of properties. This method retrieves the total number of properties available so that the other methods of the <b>Playlist</b> object can access them.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="/windows/desktop/WMP/attribute-reference">Attribute Reference</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>