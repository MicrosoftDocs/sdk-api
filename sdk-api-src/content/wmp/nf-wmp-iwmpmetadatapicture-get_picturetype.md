---
UID: NF:wmp.IWMPMetadataPicture.get_pictureType
title: IWMPMetadataPicture::get_pictureType
author: windows-sdk-content
description: The get_pictureType method retrieves a pointer to a string specifying the picture type of the metadata image.
old-location: wmp\iwmpmetadatapicture_get_picturetype.htm
tech.root: WMP
ms.assetid: 2c81d59a-9447-48bd-b95b-40e191e73a0f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPMetadataPicture interface [Windows Media Player],get_pictureType method, IWMPMetadataPicture.get_pictureType, IWMPMetadataPicture::get_pictureType, IWMPMetadataPictureget_pictureType, get_pictureType, get_pictureType method [Windows Media Player], get_pictureType method [Windows Media Player],IWMPMetadataPicture interface, wmp.iwmpmetadatapicture_get_picturetype, wmp/IWMPMetadataPicture::get_pictureType
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
 - IWMPMetadataPicture.get_pictureType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMetadataPicture::get_pictureType


## -description



The <b>get_pictureType</b> method retrieves a pointer to a string specifying the picture type of the metadata image.




## -parameters




### -param pbstrPictureType [out]

Pointer to a <b>BSTR</b> containing the picture type.


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
 

 

