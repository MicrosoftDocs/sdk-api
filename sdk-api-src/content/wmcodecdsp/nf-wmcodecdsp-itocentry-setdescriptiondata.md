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

# ITocEntry::SetDescriptionData


## -description


The <b>SetDescriptionData</b> method associates a caller-supplied data block with the entry.


## -parameters




### -param dwDescriptionDataSize [in]

The size, in bytes, of the data block.


### -param pbtDescriptionData [in]

Pointer to the first byte of the data block.


### -param pguidType [in]

Pointer to a <b>GUID</b> that identifies the type of data in the block. This parameter can be <b>NULL</b>. See Remarks.


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



You can use this method to associate any information of your choice with the entry. The nature of the information you store in the description data block is completely up to you. TOC Parser does not inspect or interpret the description data block.

You can associate only one description data block with a given entry at a given time. However, you might want to design different types of description data blocks and identfy each type of block with a globally unique identifier (GUID). That way, you could associate description data of a certain type with some of your entries and description data of a different type with other entries. If you do not need to distinguish between different types of description data blocks, you can set <i>pguidType</i> to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/4000b67c-e34e-4bce-9a0d-c56c9fc0f41e">GetDescriptionData</a>



<a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a>
 

 

