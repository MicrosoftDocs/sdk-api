---
UID: NF:wmp.IWMPMedia.isReadOnlyItem
title: IWMPMedia::isReadOnlyItem (wmp.h)
description: The isReadOnlyItem method retrieves a value indicating whether the attributes of the specified media item can be edited.helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","isReadOnlyItem method","IWMPMedia.isReadOnlyItem","IWMPMedia2 interface [Windows Media Player]","isReadOnlyItem method","IWMPMedia2::isReadOnlyItem","IWMPMedia3 interface [Windows Media Player]","isReadOnlyItem method","IWMPMedia3::isReadOnlyItem","IWMPMedia::isReadOnlyItem","IWMPMediaisReadOnlyItem","isReadOnlyItem","isReadOnlyItem method [Windows Media Player]","isReadOnlyItem method [Windows Media Player]","IWMPMedia interface","isReadOnlyItem method [Windows Media Player]","IWMPMedia2 interface","isReadOnlyItem method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_isreadonlyitem","wmp/IWMPMedia2::isReadOnlyItem","wmp/IWMPMedia3::isReadOnlyItem","wmp/IWMPMedia::isReadOnlyItem"]
old-location: wmp\iwmpmedia_isreadonlyitem.htm
tech.root: WMP
ms.assetid: d8b2dd45-3e3f-4325-b4d0-939abbc425e1
ms.date: 12/05/2018
ms.keywords: IWMPMedia interface [Windows Media Player],isReadOnlyItem method, IWMPMedia.isReadOnlyItem, IWMPMedia2 interface [Windows Media Player],isReadOnlyItem method, IWMPMedia2::isReadOnlyItem, IWMPMedia3 interface [Windows Media Player],isReadOnlyItem method, IWMPMedia3::isReadOnlyItem, IWMPMedia::isReadOnlyItem, IWMPMediaisReadOnlyItem, isReadOnlyItem, isReadOnlyItem method [Windows Media Player], isReadOnlyItem method [Windows Media Player],IWMPMedia interface, isReadOnlyItem method [Windows Media Player],IWMPMedia2 interface, isReadOnlyItem method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_isreadonlyitem, wmp/IWMPMedia2::isReadOnlyItem, wmp/IWMPMedia3::isReadOnlyItem, wmp/IWMPMedia::isReadOnlyItem
f1_keywords:
- wmp/IWMPMedia.isReadOnlyItem
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
- IWMPMedia.isReadOnlyItem
- IWMPMedia2.isReadOnlyItem
- IWMPMedia3.isReadOnlyItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMedia::isReadOnlyItem


## -description



The <b>isReadOnlyItem</b> method retrieves a value indicating whether the attributes of the specified media item can be edited.




## -parameters




### -param bstrItemName [in]

<b>BSTR</b> containing the item name.


### -param pvarfIsReadOnly [out]

Pointer to a <b>VARIANT_BOOL</b> that specifies whether the attributes are read-only.


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



If an attribute is read-only, then it cannot be set with the <b>setItemInfo</b> method. Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.

Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method always retrieves a <b>VARIANT_BOOL</b> set to <b>TRUE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-setiteminfo">IWMPMedia::setItemInfo</a>
 

 

