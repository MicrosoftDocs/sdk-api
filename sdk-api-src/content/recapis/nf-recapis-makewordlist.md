---
UID: NF:recapis.MakeWordList
title: MakeWordList function (recapis.h)
description: Creates a word list.
helpviewer_keywords: ["MakeWordList","MakeWordList function [Tablet PC]","b406a646-ab98-4852-af6d-9f4864ad8cf9","recapis/MakeWordList","tablet.makewordlist"]
old-location: tablet\makewordlist.htm
tech.root: tablet
ms.assetid: b406a646-ab98-4852-af6d-9f4864ad8cf9
ms.date: 12/05/2018
ms.keywords: MakeWordList, MakeWordList function [Tablet PC], b406a646-ab98-4852-af6d-9f4864ad8cf9, recapis/MakeWordList, tablet.makewordlist
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
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MakeWordList
 - recapis/MakeWordList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - MakeWordList
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

<a href="/windows/desktop/api/recapis/nf-recapis-addwordstowordlist">AddWordsToWordList Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-setwordlist">SetWordList Function</a>