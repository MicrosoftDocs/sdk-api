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

# IFEDictionary::RegisterWord


## -description


Registers a new word or deletes an existing word in the <a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>.


## -parameters




### -param reg [in]

Type of operation to perform. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IFED_REG_HEAD"></a><a id="ifed_reg_head"></a><dl>
<dt><b>IFED_REG_HEAD</b></dt>
</dl>
</td>
<td width="60%">
Register the word at the head of the dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_REG_TAIL"></a><a id="ifed_reg_tail"></a><dl>
<dt><b>IFED_REG_TAIL</b></dt>
</dl>
</td>
<td width="60%">
Register the word at the tail of the dictionary.

</td>
</tr>
<tr>
<td width="40%"><a id="IFED_REG_DEL"></a><a id="ifed_reg_del"></a><dl>
<dt><b>IFED_REG_DEL</b></dt>
</dl>
</td>
<td width="60%">
Delete the word from the dictionary.

</td>
</tr>
</table>
 


### -param pwrd [in]

An <a href="https://msdn.microsoft.com/BC0D039A-7EB4-4A8D-B063-479CF4294FF0">IMEWRD</a> structure specifying the word to register or delete.


## -returns



This method can return one of these values.

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
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_E_NOT_USER_DIC</b></dt>
</dl>
</td>
<td width="60%">
This <a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a> object is not a user dictionary.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_S_WORD_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The word is already registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_E_USER_COMMENT</b></dt>
</dl>
</td>
<td width="60%">
Failed to insert the user comment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failed to register or delete the word.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/BC0D039A-7EB4-4A8D-B063-479CF4294FF0">IMEWRD</a>
 

 

