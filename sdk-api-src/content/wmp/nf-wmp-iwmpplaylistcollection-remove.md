---
UID: NF:wmp.IWMPPlaylistCollection.remove
title: IWMPPlaylistCollection::remove (wmp.h)
description: The remove method removes a playlist from the library.
helpviewer_keywords: ["IWMPPlaylistCollection interface [Windows Media Player]","remove method","IWMPPlaylistCollection.remove","IWMPPlaylistCollection::remove","IWMPPlaylistCollectionremove","remove","remove method [Windows Media Player]","remove method [Windows Media Player]","IWMPPlaylistCollection interface","wmp.iwmpplaylistcollection_remove","wmp/IWMPPlaylistCollection::remove"]
old-location: wmp\iwmpplaylistcollection_remove.htm
tech.root: WMP
ms.assetid: ed678c2c-bfde-424b-9c71-21270a32a08e
ms.date: 12/05/2018
ms.keywords: IWMPPlaylistCollection interface [Windows Media Player],remove method, IWMPPlaylistCollection.remove, IWMPPlaylistCollection::remove, IWMPPlaylistCollectionremove, remove, remove method [Windows Media Player], remove method [Windows Media Player],IWMPPlaylistCollection interface, wmp.iwmpplaylistcollection_remove, wmp/IWMPPlaylistCollection::remove
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
 - IWMPPlaylistCollection::remove
 - wmp/IWMPPlaylistCollection::remove
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
 - IWMPPlaylistCollection.remove
---

# IWMPPlaylistCollection::remove


## -description

The <b>remove</b> method removes a playlist from the library.

## -parameters

### -param pItem [in]

Pointer to an <b>IWMPPlaylist</b> interface for the playlist that this method will remove.

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



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection">IWMPPlaylistCollection Interface</a>