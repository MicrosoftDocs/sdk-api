---
UID: NF:spellcheck.ISpellChecker2.Remove
title: ISpellChecker2::Remove (spellcheck.h)
description: Removes a word that was previously added by ISpellChecker.Add, or set by ISpellChecker.Ignore to be ignored.
helpviewer_keywords: ["ISpellChecker2 interface [Internationalization for Windows Applications]","Remove method","ISpellChecker2.Remove","ISpellChecker2::Remove","Remove","Remove method [Internationalization for Windows Applications]","Remove method [Internationalization for Windows Applications]","ISpellChecker2 interface","intl.ispellchecker2_remove","spellcheck/ISpellChecker2::Remove"]
old-location: intl\ispellchecker2_remove.htm
tech.root: Intl
ms.assetid: 425F1C58-D279-48E2-84D3-D3094314C756
ms.date: 12/05/2018
ms.keywords: ISpellChecker2 interface [Internationalization for Windows Applications],Remove method, ISpellChecker2.Remove, ISpellChecker2::Remove, Remove, Remove method [Internationalization for Windows Applications], Remove method [Internationalization for Windows Applications],ISpellChecker2 interface, intl.ispellchecker2_remove, spellcheck/ISpellChecker2::Remove
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ISpellChecker2::Remove
 - spellcheck/ISpellChecker2::Remove
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
 - ISpellChecker2.Remove
---

# ISpellChecker2::Remove


## -description

Removes a word that was previously added by <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add">ISpellChecker.Add</a>, or set by <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-ignore">ISpellChecker.Ignore</a> to be ignored.

## -parameters

### -param word [in]

The word to be removed from the list of added words, or from the list of ignored words. If the word is not present, nothing will be removed.

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



<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add">ISpellChecker.Add</a>



<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-ignore">ISpellChecker.Ignore</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker2">ISpellChecker2</a>