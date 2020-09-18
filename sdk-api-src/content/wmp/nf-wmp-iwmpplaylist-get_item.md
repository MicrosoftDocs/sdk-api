---
UID: NF:wmp.IWMPPlaylist.get_item
title: IWMPPlaylist::get_item (wmp.h)
description: The get_item method retrieves the media item at the specified index.
helpviewer_keywords: ["IWMPPlaylist interface [Windows Media Player]","get_item method","IWMPPlaylist.get_item","IWMPPlaylist::get_item","IWMPPlaylistget_item","get_item","get_item method [Windows Media Player]","get_item method [Windows Media Player]","IWMPPlaylist interface","wmp.iwmpplaylist_get_item","wmp/IWMPPlaylist::get_item"]
old-location: wmp\iwmpplaylist_get_item.htm
tech.root: WMP
ms.assetid: 20da6e49-720c-4291-9fb7-def441c7fc66
ms.date: 12/05/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],get_item method, IWMPPlaylist.get_item, IWMPPlaylist::get_item, IWMPPlaylistget_item, get_item, get_item method [Windows Media Player], get_item method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_get_item, wmp/IWMPPlaylist::get_item
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
 - IWMPPlaylist::get_item
 - wmp/IWMPPlaylist::get_item
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
 - IWMPPlaylist.get_item
---

# IWMPPlaylist::get_item


## -description

The <b>get_item</b> method retrieves the media item at the specified index.

## -parameters

### -param lIndex [in]

<b>long</b> containing the index.

### -param ppIWMPMedia [out]

Pointer to a pointer to an <b>IWMPMedia</b> interface for the returned item.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>