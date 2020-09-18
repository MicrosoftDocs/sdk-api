---
UID: NF:wmp.IWMPPlaylistArray.item
title: IWMPPlaylistArray::item (wmp.h)
description: The item method retrieves a pointer to an IWMPPlaylist interface representing the playlist at the specified index.
helpviewer_keywords: ["IWMPPlaylistArray interface [Windows Media Player]","item method","IWMPPlaylistArray.item","IWMPPlaylistArray::item","IWMPPlaylistArrayitem","item","item method [Windows Media Player]","item method [Windows Media Player]","IWMPPlaylistArray interface","wmp.iwmpplaylistarray_item","wmp/IWMPPlaylistArray::item"]
old-location: wmp\iwmpplaylistarray_item.htm
tech.root: WMP
ms.assetid: 2ba85800-12b9-4f14-8d68-ff6a01167308
ms.date: 12/05/2018
ms.keywords: IWMPPlaylistArray interface [Windows Media Player],item method, IWMPPlaylistArray.item, IWMPPlaylistArray::item, IWMPPlaylistArrayitem, item, item method [Windows Media Player], item method [Windows Media Player],IWMPPlaylistArray interface, wmp.iwmpplaylistarray_item, wmp/IWMPPlaylistArray::item
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
 - IWMPPlaylistArray::item
 - wmp/IWMPPlaylistArray::item
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
 - IWMPPlaylistArray.item
---

# IWMPPlaylistArray::item


## -description

The <b>item</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface representing the playlist at the specified index.

## -parameters

### -param lIndex [in]

<b>long</b> containing the index that identifies the playlist that the method should retrieve.

### -param ppItem [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the retrieved playlist.

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



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray">IWMPPlaylistArray Interface</a>