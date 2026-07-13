---
UID: NF:spellcheck.ISpellChecker.GetOptionValue
title: ISpellChecker::GetOptionValue (spellcheck.h)
description: Retrieves the value associated with the given option. (ISpellChecker.GetOptionValue)
helpviewer_keywords: ["GetOptionValue","GetOptionValue method [Internationalization for Windows Applications]","GetOptionValue method [Internationalization for Windows Applications]","ISpellChecker interface","ISpellChecker interface [Internationalization for Windows Applications]","GetOptionValue method","ISpellChecker.GetOptionValue","ISpellChecker::GetOptionValue","intl.ispellchecker_getoptionvalue","spellcheck/ISpellChecker::GetOptionValue"]
old-location: intl\ispellchecker_getoptionvalue.htm
tech.root: Intl
ms.assetid: bdbf4fa6-9827-40d5-81c0-008e166c9390
ms.date: 12/05/2018
ms.keywords: GetOptionValue, GetOptionValue method [Internationalization for Windows Applications], GetOptionValue method [Internationalization for Windows Applications],ISpellChecker interface, ISpellChecker interface [Internationalization for Windows Applications],GetOptionValue method, ISpellChecker.GetOptionValue, ISpellChecker::GetOptionValue, intl.ispellchecker_getoptionvalue, spellcheck/ISpellChecker::GetOptionValue
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
 - ISpellChecker::GetOptionValue
 - spellcheck/ISpellChecker::GetOptionValue
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
 - ISpellChecker.GetOptionValue
---

# ISpellChecker::GetOptionValue


## -description

Retrieves the value associated with the given option.

## -parameters

### -param optionId [in]

The option identifier.

### -param value [out, retval]

The value associated with <i>optionId</i>.

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
<i>optionId</i> is an empty string, or it is not one of the available options.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>optionId</i> is a null pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>
