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

# ITocEntry::GetDescriptionData


## -description


The <b>GetDescriptionData</b> method gets a description data block that was previously associated with the entry by a call to <a href="https://msdn.microsoft.com/260d7699-cf75-4179-9f2b-bc3bc49c94e6">SetDescriptionData</a>.


## -parameters




### -param pdwDescriptionDataSize [in, out]

If <i>pbtDescriptionData</i> is <b>NULL</b>, this is an output parameter that receives the size, in bytes, of the description data block. If <i>pbtDescriptionData</i> is not <b>NULL</b>, this is an input parameter that specifies the size, in bytes, of the caller-allocated buffer pointed to by <i>pbtDescriptionData</i>.


### -param pbtDescriptionData [out]

NULL, or a pointer to a caller-allocated buffer that, on successful completion, receives the description data block.


### -param pGuidType [out]

Pointer to a variable that receives a globally unique identifier (GUID) that identifies the type of data in the description data block. See Remarks.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The method returns this error code if <i>pbtDescriptionData</i> is not <b>NULL</b> and the context block is larger than the size specified by <i>pdwDescriptionDataSize</i>. In that case, <i>pdwDescriptionDataSize</i> serves as an output parameter and receives the size, in bytes, of the required buffer.

</td>
</tr>
</table>
 




## -remarks



You can associate only one description data block with a given entry at a given time. However, you might want to design different types of description data blocks and identfy each type of block with a globally unique identifier (GUID). That way, when you call <a href="https://msdn.microsoft.com/260d7699-cf75-4179-9f2b-bc3bc49c94e6">SetDescriptionData</a>, you can mark the data block as being of a specific type. When you call <b>GetDescriptionData</b>, you can determine the type of the data block retrieved by inspecting the value returned in <i>pGuidType</i>.




## -see-also




<a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a>



<a href="https://msdn.microsoft.com/260d7699-cf75-4179-9f2b-bc3bc49c94e6">SetDescriptionData</a>
 

 

