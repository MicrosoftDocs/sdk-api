---
UID: NF:spellcheckprovider.ISpellCheckProviderFactory.CreateSpellCheckProvider
title: ISpellCheckProviderFactory::CreateSpellCheckProvider (spellcheckprovider.h)
description: Creates a spell checker (implemented by a spell check provider) that supports the specified language.
helpviewer_keywords: ["CreateSpellCheckProvider","CreateSpellCheckProvider method [Internationalization for Windows Applications]","CreateSpellCheckProvider method [Internationalization for Windows Applications]","ISpellCheckProviderFactory interface","ISpellCheckProviderFactory interface [Internationalization for Windows Applications]","CreateSpellCheckProvider method","ISpellCheckProviderFactory.CreateSpellCheckProvider","ISpellCheckProviderFactory::CreateSpellCheckProvider","intl.ispellcheckproviderfactory_createspellcheckprovider","spellcheckprovider/ISpellCheckProviderFactory::CreateSpellCheckProvider"]
old-location: intl\ispellcheckproviderfactory_createspellcheckprovider.htm
tech.root: Intl
ms.assetid: E56E13D5-A41D-41F4-8E63-55664F6A8E28
ms.date: 12/05/2018
ms.keywords: CreateSpellCheckProvider, CreateSpellCheckProvider method [Internationalization for Windows Applications], CreateSpellCheckProvider method [Internationalization for Windows Applications],ISpellCheckProviderFactory interface, ISpellCheckProviderFactory interface [Internationalization for Windows Applications],CreateSpellCheckProvider method, ISpellCheckProviderFactory.CreateSpellCheckProvider, ISpellCheckProviderFactory::CreateSpellCheckProvider, intl.ispellcheckproviderfactory_createspellcheckprovider, spellcheckprovider/ISpellCheckProviderFactory::CreateSpellCheckProvider
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
 - ISpellCheckProviderFactory::CreateSpellCheckProvider
 - spellcheckprovider/ISpellCheckProviderFactory::CreateSpellCheckProvider
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
 - ISpellCheckProviderFactory.CreateSpellCheckProvider
---

# ISpellCheckProviderFactory::CreateSpellCheckProvider


## -description

Creates a spell checker (implemented by a spell check provider) that supports the specified language. This interface is not used directly by clients, but by the Spell Checking API.

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

<a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckproviderfactory-issupported">ISpellCheckProviderFactory::IsSupported</a> can be called to determine if <i>languageTag</i> is supported.

## -see-also

<a href="http://tools.ietf.org/html/bcp47">BCP47 Tags for Identifying Languages</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckproviderfactory">ISpellCheckProviderFactory</a>



<a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckproviderfactory-issupported">ISpellCheckProviderFactory::IsSupported</a>