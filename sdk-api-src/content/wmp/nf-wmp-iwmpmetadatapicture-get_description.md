---
UID: NF:wmp.IWMPMetadataPicture.get_description
title: IWMPMetadataPicture::get_description (wmp.h)
description: The get_description method retrieves a pointer to the description of the metadata image.
helpviewer_keywords: ["IWMPMetadataPicture interface [Windows Media Player]","get_description method","IWMPMetadataPicture.get_description","IWMPMetadataPicture::get_description","IWMPMetadataPictureget_description","get_description","get_description method [Windows Media Player]","get_description method [Windows Media Player]","IWMPMetadataPicture interface","wmp.iwmpmetadatapicture_get_description","wmp/IWMPMetadataPicture::get_description"]
old-location: wmp\iwmpmetadatapicture_get_description.htm
tech.root: WMP
ms.assetid: b8003560-d80d-4e0a-a6a9-88d908245477
ms.date: 12/05/2018
ms.keywords: IWMPMetadataPicture interface [Windows Media Player],get_description method, IWMPMetadataPicture.get_description, IWMPMetadataPicture::get_description, IWMPMetadataPictureget_description, get_description, get_description method [Windows Media Player], get_description method [Windows Media Player],IWMPMetadataPicture interface, wmp.iwmpmetadatapicture_get_description, wmp/IWMPMetadataPicture::get_description
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
 - IWMPMetadataPicture::get_description
 - wmp/IWMPMetadataPicture::get_description
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
 - IWMPMetadataPicture.get_description
---

# IWMPMetadataPicture::get_description


## -description

The <b>get_description</b> method retrieves a pointer to the description of the metadata image.

## -parameters

### -param pbstrDescription [out]

Pointer to a <b>BSTR</b> containing the description.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture">IWMPMetadataPicture Interface</a>