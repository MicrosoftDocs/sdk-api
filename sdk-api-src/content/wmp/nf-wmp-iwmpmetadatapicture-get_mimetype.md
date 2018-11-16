---
UID: NF:wmp.IWMPMetadataPicture.get_mimeType
title: IWMPMetadataPicture::get_mimeType
author: windows-sdk-content
description: The get_mimeType method retrieves a pointer to a string specifying the MIME type of the metadata image.
old-location: wmp\iwmpmetadatapicture_get_mimetype.htm
tech.root: WMP
ms.assetid: bfc5243f-3f7c-4f4a-9057-7720c862a983
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPMetadataPicture interface [Windows Media Player],get_mimeType method, IWMPMetadataPicture.get_mimeType, IWMPMetadataPicture::get_mimeType, IWMPMetadataPictureget_mimeType, get_mimeType, get_mimeType method [Windows Media Player], get_mimeType method [Windows Media Player],IWMPMetadataPicture interface, wmp.iwmpmetadatapicture_get_mimetype, wmp/IWMPMetadataPicture::get_mimeType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPMetadataPicture.get_mimeType
: 
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



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/385819d0-cf27-4f39-86be-140d1bc87d12">IWMPMetadataPicture Interface</a>
 

 

