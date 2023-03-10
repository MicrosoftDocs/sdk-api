---
UID: NF:wmp.IWMPStringCollection.item
title: IWMPStringCollection::item (wmp.h)
description: The item method retrieves the string at the given index.
helpviewer_keywords: ["IWMPStringCollection interface [Windows Media Player]","item method","IWMPStringCollection.item","IWMPStringCollection::item","IWMPStringCollectionitem","item","item method [Windows Media Player]","item method [Windows Media Player]","IWMPStringCollection interface","wmp.iwmpstringcollection_item","wmp/IWMPStringCollection::item"]
old-location: wmp\iwmpstringcollection_item.htm
tech.root: WMP
ms.assetid: 05e7fd0c-1226-4680-a9aa-543111fd2bdf
ms.date: 12/05/2018
ms.keywords: IWMPStringCollection interface [Windows Media Player],item method, IWMPStringCollection.item, IWMPStringCollection::item, IWMPStringCollectionitem, item, item method [Windows Media Player], item method [Windows Media Player],IWMPStringCollection interface, wmp.iwmpstringcollection_item, wmp/IWMPStringCollection::item
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
 - IWMPStringCollection::item
 - wmp/IWMPStringCollection::item
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
 - IWMPStringCollection.item
---

# IWMPStringCollection::item


## -description

The <b>item</b> method retrieves the string at the given index.

## -parameters

### -param lIndex [in]

<b>long</b> containing the index.

### -param pbstrString [out]

Pointer to a <b>BSTR</b> containing the string.

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

The <b>IWMPStringCollection</b> interface is used to retrieve the set of values available for an attribute. For example, the <b>IWMPMediaCollection::getAttributeStringCollection</b> method can be used to retrieve a pointer to an <b>IWMPStringCollection</b> interface representing all the values for the Genre attribute within the Audio media type. The <b>item</b> method can then be used to iterate through all of the possible values for the Genre attribute.

To use this method, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection">IWMPMediaCollection::getAttributeStringCollection</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection">IWMPStringCollection Interface</a>