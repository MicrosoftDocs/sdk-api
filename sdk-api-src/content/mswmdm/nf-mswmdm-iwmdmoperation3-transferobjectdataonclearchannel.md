---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IWMDMOperation3::TransferObjectDataOnClearChannel


## -description


The <b>TransferObjectDataOnClearChannel</b> method is a more efficient implementation of <a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a>.


## -parameters




### -param pData

Pointer to an unencrypted byte buffer.


### -param pdwSize

Pointer to a variable specifying the buffer size.


## -returns



The application should return one of the following <b>HRESULT</b> values.

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
The read operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The read operation should be cancelled without finishing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred, and the read operation should be cancelled without finishing.

</td>
</tr>
</table>
 




## -remarks



If the application supports this method, it is called in preference to the <b>TransferObjectData</b>.

See <b>TransferObjectData</b> to learn about the basics of this function. The difference between this method and <b>TransferObjectData</b> is that this method does not require the sender or receiver to encrypt or decrypt data, which requires extra processing time. Licensed content can still be sent using this method, since the content is always encrypted during transport anyway.

If the application supports this method, it is called in preference to the <b>TransferObjectData</b>.




## -see-also




<a href="https://msdn.microsoft.com/5ab4fdd2-d0bf-4e2c-b529-331ffa4c8403">IWMDMOperation3 Interface</a>
 

 

