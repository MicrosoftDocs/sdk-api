---
UID: NF:wmp.IWMPMedia3.getAttributeCountByType
title: IWMPMedia3::getAttributeCountByType (wmp.h)
description: The getAttributeCountByType method retrieves the number of attributes associated with the specified attribute type.
helpviewer_keywords: ["IWMPMedia3 interface [Windows Media Player]","getAttributeCountByType method","IWMPMedia3.getAttributeCountByType","IWMPMedia3::getAttributeCountByType","IWMPMedia3getAttributeCountByType","getAttributeCountByType","getAttributeCountByType method [Windows Media Player]","getAttributeCountByType method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia3_getattributecountbytype","wmp/IWMPMedia3::getAttributeCountByType"]
old-location: wmp\iwmpmedia3_getattributecountbytype.htm
tech.root: WMP
ms.assetid: 86f5e67a-408f-4b93-b89a-12f42fd31966
ms.date: 12/05/2018
ms.keywords: IWMPMedia3 interface [Windows Media Player],getAttributeCountByType method, IWMPMedia3.getAttributeCountByType, IWMPMedia3::getAttributeCountByType, IWMPMedia3getAttributeCountByType, getAttributeCountByType, getAttributeCountByType method [Windows Media Player], getAttributeCountByType method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia3_getattributecountbytype, wmp/IWMPMedia3::getAttributeCountByType
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
 - IWMPMedia3::getAttributeCountByType
 - wmp/IWMPMedia3::getAttributeCountByType
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
 - IWMPMedia3.getAttributeCountByType
---

# IWMPMedia3::getAttributeCountByType


## -description

The <b>getAttributeCountByType</b> method retrieves the number of attributes associated with the specified attribute type.

## -parameters

### -param bstrType [in]

<b>BSTR</b> containing the type.

### -param bstrLanguage [in]

<b>BSTR</b> containing the language. If the value is set to null or "" (empty string), the current locale string is used. Otherwise, the value must be a valid RFC 1766 language string such as "en-us".

### -param plCount [out]

Pointer to a <b>long</b> containing the count of attributes that are associated with the type.

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

This method is used to determine the number of attributes corresponding to a particular attribute name for a given media item. Index numbers can then be passed to the <b>getItemInfoByType</b> method. This is useful, for example, when a media item has been categorized under multiple genres.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method always retrieves a <b>long</b> set to 0.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia3">IWMPMedia3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype">IWMPMedia3::getItemInfoByType</a>