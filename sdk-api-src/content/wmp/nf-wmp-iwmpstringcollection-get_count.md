---
UID: NF:wmp.IWMPStringCollection.get_count
title: IWMPStringCollection::get_count (wmp.h)
description: The get_count method retrieves the number of items in the string collection.
helpviewer_keywords: ["IWMPStringCollection interface [Windows Media Player]","get_count method","IWMPStringCollection.get_count","IWMPStringCollection::get_count","IWMPStringCollectionget_count","get_count","get_count method [Windows Media Player]","get_count method [Windows Media Player]","IWMPStringCollection interface","wmp.iwmpstringcollection_get_count","wmp/IWMPStringCollection::get_count"]
old-location: wmp\iwmpstringcollection_get_count.htm
tech.root: WMP
ms.assetid: 97865752-e4bf-4f91-b481-22d9c8b3e090
ms.date: 12/05/2018
ms.keywords: IWMPStringCollection interface [Windows Media Player],get_count method, IWMPStringCollection.get_count, IWMPStringCollection::get_count, IWMPStringCollectionget_count, get_count, get_count method [Windows Media Player], get_count method [Windows Media Player],IWMPStringCollection interface, wmp.iwmpstringcollection_get_count, wmp/IWMPStringCollection::get_count
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
 - IWMPStringCollection::get_count
 - wmp/IWMPStringCollection::get_count
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
 - IWMPStringCollection.get_count
---

# IWMPStringCollection::get_count


## -description

The <b>get_count</b> method retrieves the number of items in the string collection.

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

To retrieve the value of this method, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection">IWMPStringCollection Interface</a>