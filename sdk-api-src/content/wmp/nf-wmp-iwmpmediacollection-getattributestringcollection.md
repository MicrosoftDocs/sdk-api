---
UID: NF:wmp.IWMPMediaCollection.getAttributeStringCollection
title: IWMPMediaCollection::getAttributeStringCollection (wmp.h)
description: The getAttributeStringCollection method retrieves a pointer to an IWMPStringCollection interface. This interface represents the set of all values for a given attribute within a given media type.
helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","getAttributeStringCollection method","IWMPMediaCollection.getAttributeStringCollection","IWMPMediaCollection::getAttributeStringCollection","IWMPMediaCollectiongetAttributeStringCollection","getAttributeStringCollection","getAttributeStringCollection method [Windows Media Player]","getAttributeStringCollection method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_getattributestringcollection","wmp/IWMPMediaCollection::getAttributeStringCollection"]
old-location: wmp\iwmpmediacollection_getattributestringcollection.htm
tech.root: WMP
ms.assetid: c3699acb-58a1-4efa-a42c-c84534abca96
ms.date: 12/05/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getAttributeStringCollection method, IWMPMediaCollection.getAttributeStringCollection, IWMPMediaCollection::getAttributeStringCollection, IWMPMediaCollectiongetAttributeStringCollection, getAttributeStringCollection, getAttributeStringCollection method [Windows Media Player], getAttributeStringCollection method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getattributestringcollection, wmp/IWMPMediaCollection::getAttributeStringCollection
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
 - IWMPMediaCollection::getAttributeStringCollection
 - wmp/IWMPMediaCollection::getAttributeStringCollection
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
 - IWMPMediaCollection.getAttributeStringCollection
---

# IWMPMediaCollection::getAttributeStringCollection


## -description

The <b>getAttributeStringCollection</b> method retrieves a pointer to an <b>IWMPStringCollection</b> interface. This interface represents the set of all values for a given attribute within a given media type.

## -parameters

### -param bstrAttribute [in]

String containing the attribute for which the values are retrieved.

### -param bstrMediaType [in]

String containing the media type for which the values are retrieved.

### -param ppStringCollection [out]

Pointer to a pointer to an <b>IWMPStringCollection</b> interface for the retrieved values.

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

For information about the attributes supported by Windows Media Player, see the <a href="/windows/desktop/WMP/attribute-reference">Attribute Reference</a> section.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection">IWMPStringCollection Interface</a>