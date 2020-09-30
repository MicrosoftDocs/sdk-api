---
UID: NF:wmp.IWMPPlaylist.setItemInfo
title: IWMPPlaylist::setItemInfo (wmp.h)
description: The setItemInfo method specifies the value of an attribute of the current playlist. .
helpviewer_keywords: ["IWMPPlaylist interface [Windows Media Player]","setItemInfo method","IWMPPlaylist.setItemInfo","IWMPPlaylist::setItemInfo","IWMPPlaylistsetItemInfo","setItemInfo","setItemInfo method [Windows Media Player]","setItemInfo method [Windows Media Player]","IWMPPlaylist interface","wmp.iwmpplaylist_setiteminfo","wmp/IWMPPlaylist::setItemInfo"]
old-location: wmp\iwmpplaylist_setiteminfo.htm
tech.root: WMP
ms.assetid: fd812af6-0bdf-4da4-a066-4411d0d9e259
ms.date: 12/05/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],setItemInfo method, IWMPPlaylist.setItemInfo, IWMPPlaylist::setItemInfo, IWMPPlaylistsetItemInfo, setItemInfo, setItemInfo method [Windows Media Player], setItemInfo method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_setiteminfo, wmp/IWMPPlaylist::setItemInfo
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
 - IWMPPlaylist::setItemInfo
 - wmp/IWMPPlaylist::setItemInfo
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
 - IWMPPlaylist.setItemInfo
---

# IWMPPlaylist::setItemInfo


## -description

The <b>setItemInfo</b> method specifies the value of an attribute of the current playlist. .

## -parameters

### -param bstrName [in]

String containing the attribute name.

### -param bstrValue [in]

String containing the attribute value.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-getiteminfo">IWMPPlaylist::getItemInfo</a>