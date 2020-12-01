---
UID: NF:spellcheck.ISpellChecker.ComprehensiveCheck
title: ISpellChecker::ComprehensiveCheck (spellcheck.h)
description: Checks the spelling of the supplied text in a more thorough manner than ISpellChecker::Check, and returns a collection of spelling errors.
helpviewer_keywords: ["ComprehensiveCheck","ComprehensiveCheck method [Internationalization for Windows Applications]","ComprehensiveCheck method [Internationalization for Windows Applications]","ISpellChecker interface","ISpellChecker interface [Internationalization for Windows Applications]","ComprehensiveCheck method","ISpellChecker.ComprehensiveCheck","ISpellChecker::ComprehensiveCheck","intl.ispellchecker_comprehensivecheck","spellcheck/ISpellChecker::ComprehensiveCheck"]
old-location: intl\ispellchecker_comprehensivecheck.htm
tech.root: Intl
ms.assetid: E364F423-AF17-4F91-993B-CEA0E50CAF67
ms.date: 12/05/2018
ms.keywords: ComprehensiveCheck, ComprehensiveCheck method [Internationalization for Windows Applications], ComprehensiveCheck method [Internationalization for Windows Applications],ISpellChecker interface, ISpellChecker interface [Internationalization for Windows Applications],ComprehensiveCheck method, ISpellChecker.ComprehensiveCheck, ISpellChecker::ComprehensiveCheck, intl.ispellchecker_comprehensivecheck, spellcheck/ISpellChecker::ComprehensiveCheck
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
 - ISpellChecker::ComprehensiveCheck
 - spellcheck/ISpellChecker::ComprehensiveCheck
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
 - ISpellChecker.ComprehensiveCheck
---

# ISpellChecker::ComprehensiveCheck


## -description

Checks the spelling of the supplied text in a more thorough manner than <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-check">ISpellChecker::Check</a>, and returns a collection of spelling errors.

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

The returned <a href="/windows/desktop/api/spellcheck/nn-spellcheck-ienumspellingerror">IEnumSpellingError</a> contains the results of spell checking. A correct <i>text</i> returns an empty (not a null) enumeration.

If the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it implements <a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider">IComprehensiveSpellCheckProvider</a> to support the more thorough checking mode. 
When a client calls <b>ISpellChecker::ComprehensiveCheck</b>, the spell checking functionality will <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> the provider for <b>IComprehensiveSpellCheckProvider</b>, and call <a href="/windows/desktop/Intl/icomprehensivespellcheckprovider-comprehensivecheck">IComprehensiveSpellCheckProvider.ComprehensiveCheck</a> if the interface is supported. If the interface isn't supported, it will silently fall back to <a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check">ISpellCheckProvider::Check</a>.

## -see-also

<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider">IComprehensiveSpellCheckProvider</a>



<a href="/windows/desktop/Intl/icomprehensivespellcheckprovider-comprehensivecheck">IComprehensiveSpellCheckProvider.ComprehensiveCheck</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ienumspellingerror">IEnumSpellingError</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>



<a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check">ISpellCheckProvider::Check</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>