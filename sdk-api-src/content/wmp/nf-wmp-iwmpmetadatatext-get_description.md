---
UID: NF:wmp.IWMPMetadataText.get_description
title: IWMPMetadataText::get_description (wmp.h)
description: The get_description method retrieves a description of the metadata text.
helpviewer_keywords: ["IWMPMetadataText interface [Windows Media Player]","get_description method","IWMPMetadataText.get_description","IWMPMetadataText::get_description","IWMPMetadataTextget_description","get_description","get_description method [Windows Media Player]","get_description method [Windows Media Player]","IWMPMetadataText interface","wmp.iwmpmetadatatext_get_description","wmp/IWMPMetadataText::get_description"]
old-location: wmp\iwmpmetadatatext_get_description.htm
tech.root: WMP
ms.assetid: 8a593336-7ec8-4238-8923-c65374cecbeb
ms.date: 12/05/2018
ms.keywords: IWMPMetadataText interface [Windows Media Player],get_description method, IWMPMetadataText.get_description, IWMPMetadataText::get_description, IWMPMetadataTextget_description, get_description, get_description method [Windows Media Player], get_description method [Windows Media Player],IWMPMetadataText interface, wmp.iwmpmetadatatext_get_description, wmp/IWMPMetadataText::get_description
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
 - IWMPMetadataText::get_description
 - wmp/IWMPMetadataText::get_description
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
 - IWMPMetadataText.get_description
---

# IWMPMetadataText::get_description


## -description

The <b>get_description</b> method retrieves a description of the metadata text.

## -parameters

### -param pbstrDescription [out]

Pointer to a BSTR containing the description.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext">IWMPMetadataText Interface</a>