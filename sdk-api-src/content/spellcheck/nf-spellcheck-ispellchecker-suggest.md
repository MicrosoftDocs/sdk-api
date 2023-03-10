---
UID: NF:spellcheck.ISpellChecker.Suggest
title: ISpellChecker::Suggest (spellcheck.h)
description: Retrieves spelling suggestions for the supplied text. (ISpellChecker.Suggest)
helpviewer_keywords: ["ISpellChecker interface [Internationalization for Windows Applications]","Suggest method","ISpellChecker.Suggest","ISpellChecker::Suggest","Suggest","Suggest method [Internationalization for Windows Applications]","Suggest method [Internationalization for Windows Applications]","ISpellChecker interface","intl.ispellchecker_suggest","spellcheck/ISpellChecker::Suggest"]
old-location: intl\ispellchecker_suggest.htm
tech.root: Intl
ms.assetid: bd6b1d90-8dc0-4640-a43a-678b43e55cb5
ms.date: 12/05/2018
ms.keywords: ISpellChecker interface [Internationalization for Windows Applications],Suggest method, ISpellChecker.Suggest, ISpellChecker::Suggest, Suggest, Suggest method [Internationalization for Windows Applications], Suggest method [Internationalization for Windows Applications],ISpellChecker interface, intl.ispellchecker_suggest, spellcheck/ISpellChecker::Suggest
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
 - ISpellChecker::Suggest
 - spellcheck/ISpellChecker::Suggest
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
 - ISpellChecker.Suggest
---

# ISpellChecker::Suggest


## -description

Retrieves spelling suggestions for the supplied text.

## -parameters

### -param word [in]

The word or phrase to get suggestions for.

### -param value [out, retval]

The list of suggestions, returned as an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> object.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is correctly spelled. <i>value</i> contains one entry, which is the text that was passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is an empty string.

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

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>
