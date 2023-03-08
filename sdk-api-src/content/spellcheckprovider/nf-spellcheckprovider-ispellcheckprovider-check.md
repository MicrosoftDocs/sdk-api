---
UID: NF:spellcheckprovider.ISpellCheckProvider.Check
title: ISpellCheckProvider::Check (spellcheckprovider.h)
description: Checks the spelling of the supplied text and returns a collection of spelling errors. (ISpellCheckProvider.Check)
helpviewer_keywords: ["Check","Check method [Internationalization for Windows Applications]","Check method [Internationalization for Windows Applications]","ISpellCheckProvider interface","ISpellCheckProvider interface [Internationalization for Windows Applications]","Check method","ISpellCheckProvider.Check","ISpellCheckProvider::Check","intl.ispellcheckprovider_check","spellcheckprovider/ISpellCheckProvider::Check"]
old-location: intl\ispellcheckprovider_check.htm
tech.root: Intl
ms.assetid: B8C62B56-FF72-4C94-AC77-A6BEFCFE2589
ms.date: 12/05/2018
ms.keywords: Check, Check method [Internationalization for Windows Applications], Check method [Internationalization for Windows Applications],ISpellCheckProvider interface, ISpellCheckProvider interface [Internationalization for Windows Applications],Check method, ISpellCheckProvider.Check, ISpellCheckProvider::Check, intl.ispellcheckprovider_check, spellcheckprovider/ISpellCheckProvider::Check
req.header: spellcheckprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheckprovider.idl
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
 - ISpellCheckProvider::Check
 - spellcheckprovider/ISpellCheckProvider::Check
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheckprovider.h
api_name:
 - ISpellCheckProvider.Check
---

# ISpellCheckProvider::Check


## -description

Checks the spelling of the supplied text and returns a collection of spelling errors.

## -parameters

### -param text [in]

The text to check.

### -param value [out, retval]

The result of checking this text, returned as an <a href="/windows/desktop/api/spellcheck/nn-spellcheck-ienumspellingerror">IEnumSpellingError</a> object.

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
<i>text</i> is an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>text</i> is a null pointer.

</td>
</tr>
</table>

## -remarks

The returned <a href="/windows/desktop/api/spellcheck/nn-spellcheck-ienumspellingerror">IEnumSpellingError</a> should contain the results of spell checking. A correct <i>text</i> should return an empty (not a null) enumeration.

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ienumspellingerror">IEnumSpellingError</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>
