---
UID: NF:spellcheckprovider.ISpellCheckProviderFactory.IsSupported
title: ISpellCheckProviderFactory::IsSupported (spellcheckprovider.h)
description: Determines if the specified language is supported by this spell checker.
helpviewer_keywords: ["ISpellCheckProviderFactory interface [Internationalization for Windows Applications]","IsSupported method","ISpellCheckProviderFactory.IsSupported","ISpellCheckProviderFactory::IsSupported","IsSupported","IsSupported method [Internationalization for Windows Applications]","IsSupported method [Internationalization for Windows Applications]","ISpellCheckProviderFactory interface","intl.ispellcheckproviderfactory_issupported","spellcheckprovider/ISpellCheckProviderFactory::IsSupported"]
old-location: intl\ispellcheckproviderfactory_issupported.htm
tech.root: Intl
ms.assetid: 88689384-E95E-4D56-BAD4-9889816F76EB
ms.date: 12/05/2018
ms.keywords: ISpellCheckProviderFactory interface [Internationalization for Windows Applications],IsSupported method, ISpellCheckProviderFactory.IsSupported, ISpellCheckProviderFactory::IsSupported, IsSupported, IsSupported method [Internationalization for Windows Applications], IsSupported method [Internationalization for Windows Applications],ISpellCheckProviderFactory interface, intl.ispellcheckproviderfactory_issupported, spellcheckprovider/ISpellCheckProviderFactory::IsSupported
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
 - ISpellCheckProviderFactory::IsSupported
 - spellcheckprovider/ISpellCheckProviderFactory::IsSupported
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
 - ISpellCheckProviderFactory.IsSupported
---

# ISpellCheckProviderFactory::IsSupported


## -description

Determines if the specified language is supported by this spell checker.

## -parameters

### -param languageTag [in]

A <a href="http://tools.ietf.org/html/bcp47">BCP47</a> language tag that identifies the language for the requested spell checker.

### -param value [out, retval]

<b>TRUE</b> if supported; <b>FALSE</b> if not supported.

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
<i>languageTag</i> is an empty string.

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

## -see-also

<a href="http://tools.ietf.org/html/bcp47">BCP47 Tags for Identifying Languages

</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckproviderfactory">ISpellCheckProviderFactory</a>