---
UID: NF:spellcheck.ISpellChecker.Add
title: ISpellChecker::Add (spellcheck.h)
description: Treats the provided word as though it were part of the original dictionary.
helpviewer_keywords: ["Add","Add method [Internationalization for Windows Applications]","Add method [Internationalization for Windows Applications]","ISpellChecker interface","ISpellChecker interface [Internationalization for Windows Applications]","Add method","ISpellChecker.Add","ISpellChecker::Add","intl.ispellchecker_add","spellcheck/ISpellChecker::Add"]
old-location: intl\ispellchecker_add.htm
tech.root: Intl
ms.assetid: d600a57e-7191-4a82-8004-026a04ef94ed
ms.date: 12/05/2018
ms.keywords: Add, Add method [Internationalization for Windows Applications], Add method [Internationalization for Windows Applications],ISpellChecker interface, ISpellChecker interface [Internationalization for Windows Applications],Add method, ISpellChecker.Add, ISpellChecker::Add, intl.ispellchecker_add, spellcheck/ISpellChecker::Add
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheck.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpellChecker::Add
 - spellcheck/ISpellChecker::Add
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheck.h
api_name:
 - ISpellChecker.Add
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

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>