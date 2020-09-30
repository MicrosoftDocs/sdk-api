---
UID: NF:spellcheckprovider.IComprehensiveSpellCheckProvider.ComprehensiveCheck
title: IComprehensiveSpellCheckProvider::ComprehensiveCheck (spellcheckprovider.h)
description: Spell-check the provider text in a more thorough manner than ISpellCheckProvider::Check.
helpviewer_keywords: ["ComprehensiveCheck","ComprehensiveCheck method [Internationalization for Windows Applications]","ComprehensiveCheck method [Internationalization for Windows Applications]","IComprehensiveSpellCheckProvider interface","IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications]","ComprehensiveCheck method","IComprehensiveSpellCheckProvider.ComprehensiveCheck","IComprehensiveSpellCheckProvider::ComprehensiveCheck","intl.icomprehensivespellcheckprovider_comprehensivecheck","spellcheckprovider/IComprehensiveSpellCheckProvider::ComprehensiveCheck"]
old-location: intl\icomprehensivespellcheckprovider_comprehensivecheck.htm
tech.root: Intl
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
ms.date: 12/05/2018
ms.keywords: ComprehensiveCheck, ComprehensiveCheck method [Internationalization for Windows Applications], ComprehensiveCheck method [Internationalization for Windows Applications],IComprehensiveSpellCheckProvider interface, IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications],ComprehensiveCheck method, IComprehensiveSpellCheckProvider.ComprehensiveCheck, IComprehensiveSpellCheckProvider::ComprehensiveCheck, intl.icomprehensivespellcheckprovider_comprehensivecheck, spellcheckprovider/IComprehensiveSpellCheckProvider::ComprehensiveCheck
req.header: spellcheckprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IComprehensiveSpellCheckProvider::ComprehensiveCheck
 - spellcheckprovider/IComprehensiveSpellCheckProvider::ComprehensiveCheck
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spellcheckprovider.h
api_name:
 - IComprehensiveSpellCheckProvider.ComprehensiveCheck
---

# IComprehensiveSpellCheckProvider::ComprehensiveCheck


## -description

Spell-check the provider text in a more thorough manner than <a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check">ISpellCheckProvider::Check</a>.

## -parameters

### -param text [in]

The text to check.

### -param value [out]

The result of checking this text, as an enumeration of spelling errors (<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ienumspellingerror">IEnumSpellingError</a>), if any.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
<i>text</i> is an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<i>text</i> is a null pointer.

</td>
</tr>
</table>

## -remarks

This interface isn't required to be implemented by a spell check provider. But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements <a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a> to support the more thorough checking mode. 
When a client calls <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck">ISpellChecker::ComprehensiveCheck</a>, the spell checking functionality will <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> the provider for <a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider">IComprehensiveSpellCheckProvider</a>, and call <b>IComprehensiveSpellCheckProvider.ComprehensiveCheck</b> if the interface is supported. If the interface isn't supported, it will silently fall back to <a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check">ISpellCheckProvider::Check</a>.

## -see-also

<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider">IComprehensiveSpellCheckProvider</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ienumspellingerror">IEnumSpellingError</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>



<a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check">ISpellCheckProvider::Check</a>



<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck">ISpellChecker::ComprehensiveCheck</a>