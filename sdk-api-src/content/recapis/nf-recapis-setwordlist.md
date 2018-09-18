---
UID: NF:recapis.SetWordList
title: SetWordList function
author: windows-sdk-content
description: Sets the word list for the current recognizer context to recognize.
old-location: tablet\setwordlist.htm
tech.root: tablet
ms.assetid: 9e067c22-772d-48d2-baae-abc8067efb09
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 9e067c22-772d-48d2-baae-abc8067efb09, SetWordList, SetWordList function [Tablet PC], recapis/SetWordList, tablet.setwordlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - SetWordList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
The method was called after <a href="https://msdn.microsoft.com/564a2734-1a90-4566-a39d-7e16eff870ff">Process</a> has been called.

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
 

 

