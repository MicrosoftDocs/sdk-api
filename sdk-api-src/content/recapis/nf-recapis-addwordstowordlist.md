---
UID: NF:recapis.AddWordsToWordList
title: AddWordsToWordList function (recapis.h)
description: Adds one or more words to the word list.
helpviewer_keywords: ["8487bdad-c927-44dc-b757-40a0aba285ca","AddWordsToWordList","AddWordsToWordList function [Tablet PC]","recapis/AddWordsToWordList","tablet.addwordstowordlist"]
old-location: tablet\addwordstowordlist.htm
tech.root: tablet
ms.assetid: 8487bdad-c927-44dc-b757-40a0aba285ca
ms.date: 12/05/2018
ms.keywords: 8487bdad-c927-44dc-b757-40a0aba285ca, AddWordsToWordList, AddWordsToWordList function [Tablet PC], recapis/AddWordsToWordList, tablet.addwordstowordlist
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
 - AddWordsToWordList
 - recapis/AddWordsToWordList
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
 - AddWordsToWordList
---

# AddWordsToWordList function


## -description

Adds one or more words to the word list.

## -parameters

### -param hwl

Handle to the word list.

### -param pwcWords

Words to add to the word list. Separate words in this list with a \0 character and end the list with two \0 characters. Words that already exist in the list are not added.

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
Returned when the word list handle parameter is invalid.

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
</table>

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-makewordlist">MakeWordList Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-setwordlist">SetWordList Function</a>