---
UID: NF:wmp.IWMPPlaylist.put_name
title: IWMPPlaylist::put_name (wmp.h)
description: The put_name method specifies the name of the playlist.
helpviewer_keywords: ["IWMPPlaylist interface [Windows Media Player]","put_name method","IWMPPlaylist.put_name","IWMPPlaylist::put_name","IWMPPlaylistput_name","put_name","put_name method [Windows Media Player]","put_name method [Windows Media Player]","IWMPPlaylist interface","wmp.iwmpplaylist_put_name","wmp/IWMPPlaylist::put_name"]
old-location: wmp\iwmpplaylist_put_name.htm
tech.root: WMP
ms.assetid: 749dae2f-d9c3-4bbb-9a2f-042388f5ce0c
ms.date: 12/05/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],put_name method, IWMPPlaylist.put_name, IWMPPlaylist::put_name, IWMPPlaylistput_name, put_name, put_name method [Windows Media Player], put_name method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_put_name, wmp/IWMPPlaylist::put_name
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
 - IWMPPlaylist::put_name
 - wmp/IWMPPlaylist::put_name
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
 - IWMPPlaylist.put_name
---

# IWMPPlaylist::put_name


## -description

The <b>put_name</b> method specifies the name of the playlist.

## -parameters

### -param bstrName [in]

String containing the name.

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

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_name">IWMPPlaylist::get_name</a>