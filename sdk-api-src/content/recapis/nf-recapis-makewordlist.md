---
UID: NF:recapis.MakeWordList
title: MakeWordList function
author: windows-driver-content
description: Creates a word list.
old-location: tablet\makewordlist.htm
old-project: tablet
ms.assetid: b406a646-ab98-4852-af6d-9f4864ad8cf9
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: MakeWordList, MakeWordList function [Tablet PC], b406a646-ab98-4852-af6d-9f4864ad8cf9, recapis/MakeWordList, tablet.makewordlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps | UWP apps]
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
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	recapis.h
api_name:
-	MakeWordList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MakeWordList function


## -description



Creates a word list.




## -parameters




### -param hrec

Handle to the recognizer.


### -param pBuffer

Words to insert into the new word list. Separate words in this list with a \0 character and end the list with two \0 characters.


### -param phwl

Handle to the new word list.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The pointer to the word list is incorrect.

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
<dt><b>TPC_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
An error is found in one of the words in the list. Possible errors include unsupported characters, spaces at the start or the end of the word or more than a single space between words. All words up to the incorrect word are added to the word list.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8487bdad-c927-44dc-b757-40a0aba285ca">AddWordsToWordList Function</a>



<a href="https://msdn.microsoft.com/9e067c22-772d-48d2-baae-abc8067efb09">SetWordList Function</a>
 

 

