---
UID: NF:wmp.IWMPMetadataText.get_text
title: IWMPMetadataText::get_text (wmp.h)
description: The get_text method retrieves the metadata text.
helpviewer_keywords: ["IWMPMetadataText interface [Windows Media Player]","get_text method","IWMPMetadataText.get_text","IWMPMetadataText::get_text","IWMPMetadataTextget_text","get_text","get_text method [Windows Media Player]","get_text method [Windows Media Player]","IWMPMetadataText interface","wmp.iwmpmetadatatext_get_text","wmp/IWMPMetadataText::get_text"]
old-location: wmp\iwmpmetadatatext_get_text.htm
tech.root: WMP
ms.assetid: 88aeb4bb-87e1-413d-888b-608fa349ebf5
ms.date: 12/05/2018
ms.keywords: IWMPMetadataText interface [Windows Media Player],get_text method, IWMPMetadataText.get_text, IWMPMetadataText::get_text, IWMPMetadataTextget_text, get_text, get_text method [Windows Media Player], get_text method [Windows Media Player],IWMPMetadataText interface, wmp.iwmpmetadatatext_get_text, wmp/IWMPMetadataText::get_text
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
 - IWMPMetadataText::get_text
 - wmp/IWMPMetadataText::get_text
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
 - IWMPMetadataText.get_text
---

# IWMPMetadataText::get_text


## -description

The <b>get_text</b> method retrieves the metadata text.

## -parameters

### -param pbstrText [out]

Pointer to a <b>BSTR</b> containing the text.

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

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext">IWMPMetadataText Interface</a>