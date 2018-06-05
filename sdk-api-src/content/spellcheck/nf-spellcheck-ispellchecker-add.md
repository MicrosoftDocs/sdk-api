---
UID: NF:spellcheck.ISpellChecker.Add
title: ISpellChecker::Add
author: windows-sdk-content
description: Treats the provided word as though it were part of the original dictionary.
old-location: intl\ispellchecker_add.htm
old-project: Intl
ms.assetid: d600a57e-7191-4a82-8004-026a04ef94ed
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Add, Add method [Internationalization for Windows Applications], Add method [Internationalization for Windows Applications],ISpellChecker interface, ISpellChecker interface [Internationalization for Windows Applications],Add method, ISpellChecker.Add, ISpellChecker::Add, intl.ispellchecker_add, spellcheck/ISpellChecker::Add
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheck.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WORDLIST_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Spellcheck.h
api_name:
-	ISpellChecker.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellChecker::Add


## -description


Treats the provided word as though it were part of the original dictionary.

The word  will no longer be considered misspelled, and will also be considered as a candidate for suggestions.


## -parameters




### -param word [in]

The word to be added to the list of added words.


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
Successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is an empty string, or its length is greater than <b>MAX_WORD_LENGTH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is a null pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>
 

 

