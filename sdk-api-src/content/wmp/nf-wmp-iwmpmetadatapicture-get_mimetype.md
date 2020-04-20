---
UID: NF:wmp.IWMPMetadataPicture.get_mimeType
title: IWMPMetadataPicture::get_mimeType (wmp.h)
description: The get_mimeType method retrieves a pointer to a string specifying the MIME type of the metadata image.helpviewer_keywords: ["IWMPMetadataPicture interface [Windows Media Player]","get_mimeType method","IWMPMetadataPicture.get_mimeType","IWMPMetadataPicture::get_mimeType","IWMPMetadataPictureget_mimeType","get_mimeType","get_mimeType method [Windows Media Player]","get_mimeType method [Windows Media Player]","IWMPMetadataPicture interface","wmp.iwmpmetadatapicture_get_mimetype","wmp/IWMPMetadataPicture::get_mimeType"]
old-location: wmp\iwmpmetadatapicture_get_mimetype.htm
tech.root: WMP
ms.assetid: bfc5243f-3f7c-4f4a-9057-7720c862a983
ms.date: 12/05/2018
ms.keywords: IWMPMetadataPicture interface [Windows Media Player],get_mimeType method, IWMPMetadataPicture.get_mimeType, IWMPMetadataPicture::get_mimeType, IWMPMetadataPictureget_mimeType, get_mimeType, get_mimeType method [Windows Media Player], get_mimeType method [Windows Media Player],IWMPMetadataPicture interface, wmp.iwmpmetadatapicture_get_mimetype, wmp/IWMPMetadataPicture::get_mimeType
f1_keywords:
- wmp/IWMPMetadataPicture.get_mimeType
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
- IWMPMetadataPicture.get_mimeType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMetadataPicture::get_mimeType


## -description



The <b>get_mimeType</b> method retrieves a pointer to a string specifying the MIME type of the metadata image.




## -parameters




### -param pbstrMimeType [out]

Pointer to a <b>BSTR</b> containing the mime type.


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



Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture">IWMPMetadataPicture Interface</a>
 

 

