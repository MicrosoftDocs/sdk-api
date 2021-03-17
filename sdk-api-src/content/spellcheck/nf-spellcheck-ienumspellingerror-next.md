---
UID: NF:spellcheck.IEnumSpellingError.Next
title: IEnumSpellingError::Next (spellcheck.h)
description: Gets the next spelling error.
helpviewer_keywords: ["IEnumSpellingError interface [Internationalization for Windows Applications]","Next method","IEnumSpellingError.Next","IEnumSpellingError::Next","Next","Next method [Internationalization for Windows Applications]","Next method [Internationalization for Windows Applications]","IEnumSpellingError interface","intl.ienumspellingerror_next","spellcheck/IEnumSpellingError::Next"]
old-location: intl\ienumspellingerror_next.htm
tech.root: Intl
ms.assetid: c0fba585-2511-4162-8232-4e0510dc9261
ms.date: 12/05/2018
ms.keywords: IEnumSpellingError interface [Internationalization for Windows Applications],Next method, IEnumSpellingError.Next, IEnumSpellingError::Next, Next, Next method [Internationalization for Windows Applications], Next method [Internationalization for Windows Applications],IEnumSpellingError interface, intl.ienumspellingerror_next, spellcheck/IEnumSpellingError::Next
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
 - IEnumSpellingError::Next
 - spellcheck/IEnumSpellingError::Next
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
 - IEnumSpellingError.Next
---

# IEnumSpellingError::Next


## -description

Gets the next spelling error.

## -parameters

### -param value [out, retval]

The spelling error (<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellingerror">ISpellingError</a>) returned.

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
There is no spelling error left to return.  <i>value</i> does not point at a valid <a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellingerror">ISpellingError</a>.

</td>
</tr>
</table>

## -remarks

If there are no spelling errors, this will return <b>S_FALSE</b>.
This provides a way for a provider to implement spell checking lazily if desired—instead of doing the spell checking work on <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-check">ISpellCheckProvider::Check</a> and getting all the errors at once, you can do it only as needed when this method is called, getting one error per call.

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ienumspellingerror">IEnumSpellingError</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellingerror">ISpellingError</a>