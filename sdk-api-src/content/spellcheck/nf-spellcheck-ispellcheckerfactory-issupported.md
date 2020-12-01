---
UID: NF:spellcheck.ISpellCheckerFactory.IsSupported
title: ISpellCheckerFactory::IsSupported (spellcheck.h)
description: Determines if the specified language is supported by a registered spell checker.
helpviewer_keywords: ["ISpellCheckerFactory interface [Internationalization for Windows Applications]","IsSupported method","ISpellCheckerFactory.IsSupported","ISpellCheckerFactory::IsSupported","IsSupported","IsSupported method [Internationalization for Windows Applications]","IsSupported method [Internationalization for Windows Applications]","ISpellCheckerFactory interface","intl.ispellcheckerfactory_issupported","spellcheck/ISpellCheckerFactory::IsSupported"]
old-location: intl\ispellcheckerfactory_issupported.htm
tech.root: Intl
ms.assetid: eb21850d-d490-4055-8910-70f9c0090f59
ms.date: 12/05/2018
ms.keywords: ISpellCheckerFactory interface [Internationalization for Windows Applications],IsSupported method, ISpellCheckerFactory.IsSupported, ISpellCheckerFactory::IsSupported, IsSupported, IsSupported method [Internationalization for Windows Applications], IsSupported method [Internationalization for Windows Applications],ISpellCheckerFactory interface, intl.ispellcheckerfactory_issupported, spellcheck/ISpellCheckerFactory::IsSupported
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
 - ISpellCheckerFactory::IsSupported
 - spellcheck/ISpellCheckerFactory::IsSupported
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
 - ISpellCheckerFactory.IsSupported
---

# ISpellCheckerFactory::IsSupported


## -description

Determines if the specified language is supported by a registered spell checker.

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



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerfactory">ISpellCheckerFactory</a>