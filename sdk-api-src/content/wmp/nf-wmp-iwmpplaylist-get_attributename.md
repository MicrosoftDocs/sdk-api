---
UID: NF:wmp.IWMPPlaylist.get_attributeName
title: IWMPPlaylist::get_attributeName (wmp.h)
description: The get_attributeName method retrieves the name of an attribute specified by an index.
helpviewer_keywords: ["IWMPPlaylist interface [Windows Media Player]","get_attributeName method","IWMPPlaylist.get_attributeName","IWMPPlaylist::get_attributeName","IWMPPlaylistget_attributeName","get_attributeName","get_attributeName method [Windows Media Player]","get_attributeName method [Windows Media Player]","IWMPPlaylist interface","wmp.iwmpplaylist_get_attributename","wmp/IWMPPlaylist::get_attributeName"]
old-location: wmp\iwmpplaylist_get_attributename.htm
tech.root: WMP
ms.assetid: 30bdf1e0-2bb8-486e-bec7-d06e1ac6ed9b
ms.date: 12/05/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],get_attributeName method, IWMPPlaylist.get_attributeName, IWMPPlaylist::get_attributeName, IWMPPlaylistget_attributeName, get_attributeName, get_attributeName method [Windows Media Player], get_attributeName method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_get_attributename, wmp/IWMPPlaylist::get_attributeName
f1_keywords:
- wmp/IWMPPlaylist.get_attributeName
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPPlaylist.get_attributeName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlaylist::get_attributeName


## -description



The <b>get_attributeName</b> method retrieves the name of an attribute specified by an index.




## -parameters




### -param lIndex [in]

<b>long</b> containing the index.


### -param pbstrAttributeName [out]

Pointer to a <b>BSTR</b> containing the attribute name.


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



The number of attributes is retrieved by the <b>get_attributeCount</b> method.

The <i>pbstAttributeName</i> string can be supplied to the <b>setItemInfo</b> or <b>getItemInfo</b> methods to specify or retrieve a value for the named attribute.

Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.

For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="https://docs.microsoft.com/windows/desktop/WMP/attribute-reference">Attribute Reference</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-getiteminfo">IWMPPlaylist::getItemInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_attributecount">IWMPPlaylist::get_attributeCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo">IWMPPlaylist::setItemInfo</a>
 

 

