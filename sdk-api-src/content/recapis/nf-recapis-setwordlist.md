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

# SetWordList function


## -description



Sets the word list for the current recognizer context to recognize.




## -parameters




### -param hrc

Handle to the recognizer context.


### -param hwl

Handle to recognition word list to be used.


## -returns



This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The context is invalid or one of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not support this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method was called after <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">Process</a> has been called.

</td>
</tr>
</table>
 




## -remarks



The word list passed in as the second parameter must already exist. You create a word list by using the <a href="https://msdn.microsoft.com/b406a646-ab98-4852-af6d-9f4864ad8cf9">MakeWordList</a> function. The <b>SetWordList</b> function does not alter the word list.

To clear the wordlist, pass <b>NULL</b> as the second parameter.

It is recommended that you limit the length of individual words in the wordlist to no more than 256 characters and limit memory allocation for wordlists to no more than 128 MB.




## -see-also




<a href="https://msdn.microsoft.com/8487bdad-c927-44dc-b757-40a0aba285ca">AddWordsToWordList Function</a>



<a href="https://msdn.microsoft.com/b406a646-ab98-4852-af6d-9f4864ad8cf9">MakeWordList Function</a>
 

 

