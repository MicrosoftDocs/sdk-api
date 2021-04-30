---
UID: NF:spellcheck.ISpellCheckerFactory.CreateSpellChecker
title: ISpellCheckerFactory::CreateSpellChecker (spellcheck.h)
description: Creates a spell checker that supports the specified language.
helpviewer_keywords: ["CreateSpellChecker","CreateSpellChecker method [Internationalization for Windows Applications]","CreateSpellChecker method [Internationalization for Windows Applications]","ISpellCheckerFactory interface","ISpellCheckerFactory interface [Internationalization for Windows Applications]","CreateSpellChecker method","ISpellCheckerFactory.CreateSpellChecker","ISpellCheckerFactory::CreateSpellChecker","intl.ispellcheckerfactory_createspellchecker","spellcheck/ISpellCheckerFactory::CreateSpellChecker"]
old-location: intl\ispellcheckerfactory_createspellchecker.htm
tech.root: Intl
ms.assetid: 9167b675-01ec-4173-a790-5452907b5598
ms.date: 12/05/2018
ms.keywords: CreateSpellChecker, CreateSpellChecker method [Internationalization for Windows Applications], CreateSpellChecker method [Internationalization for Windows Applications],ISpellCheckerFactory interface, ISpellCheckerFactory interface [Internationalization for Windows Applications],CreateSpellChecker method, ISpellCheckerFactory.CreateSpellChecker, ISpellCheckerFactory::CreateSpellChecker, intl.ispellcheckerfactory_createspellchecker, spellcheck/ISpellCheckerFactory::CreateSpellChecker
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
 - ISpellCheckerFactory::CreateSpellChecker
 - spellcheck/ISpellCheckerFactory::CreateSpellChecker
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
 - ISpellCheckerFactory.CreateSpellChecker
---

# ISpellCheckerFactory::CreateSpellChecker


## -description

Creates a spell checker that supports the specified language.

## -parameters

### -param languageTag [in]

A <a href="http://tools.ietf.org/html/bcp47">BCP47</a> language tag that identifies the language for the requested spell checker.

### -param value [out, retval]

The created spell checker.

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
<i>languageTag</i> is an empty string, or there is no spell checker available for <i>languageTag</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>languageTag</i> is a null pointer.

</td>
</tr>
</table>

## -remarks

<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellcheckerfactory-issupported">ISpellCheckerFactory::IsSupported</a> can be called to determine if <i>languageTag</i> is supported.
This will create the preferred spell checker (according to user ranking) for the given language.

## -see-also

<a href="http://tools.ietf.org/html/bcp47">BCP47 Tags for Identifying Languages</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerfactory">ISpellCheckerFactory</a>



<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellcheckerfactory-issupported">ISpellCheckerFactory::IsSupported</a>