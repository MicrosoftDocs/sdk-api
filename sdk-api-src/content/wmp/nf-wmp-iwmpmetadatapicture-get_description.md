---
UID: NF:wmp.IWMPMetadataPicture.get_description
title: IWMPMetadataPicture::get_description
author: windows-sdk-content
description: The get_description method retrieves a pointer to the description of the metadata image.
old-location: wmp\iwmpmetadatapicture_get_description.htm
old-project: WMP
ms.assetid: b8003560-d80d-4e0a-a6a9-88d908245477
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPMetadataPicture interface [Windows Media Player],get_description method, IWMPMetadataPicture.get_description, IWMPMetadataPicture::get_description, IWMPMetadataPictureget_description, get_description, get_description method [Windows Media Player], get_description method [Windows Media Player],IWMPMetadataPicture interface, wmp.iwmpmetadatapicture_get_description, wmp/IWMPMetadataPicture::get_description
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPMetadataPicture.get_description
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/385819d0-cf27-4f39-86be-140d1bc87d12">IWMPMetadataPicture Interface</a>
 

 

