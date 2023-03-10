---
UID: NF:spellcheck.ISpellChecker.GetOptionDescription
title: ISpellChecker::GetOptionDescription (spellcheck.h)
description: Retrieves the information (id, description, heading and labels) of a specific option. (ISpellChecker.GetOptionDescription)
helpviewer_keywords: ["GetOptionDescription","GetOptionDescription method [Internationalization for Windows Applications]","GetOptionDescription method [Internationalization for Windows Applications]","ISpellChecker interface","ISpellChecker interface [Internationalization for Windows Applications]","GetOptionDescription method","ISpellChecker.GetOptionDescription","ISpellChecker::GetOptionDescription","intl.ispellchecker_getoptiondescription","spellcheck/ISpellChecker::GetOptionDescription"]
old-location: intl\ispellchecker_getoptiondescription.htm
tech.root: Intl
ms.assetid: 5947f6ee-ad52-4d4d-a013-0c7dced273c3
ms.date: 12/05/2018
ms.keywords: GetOptionDescription, GetOptionDescription method [Internationalization for Windows Applications], GetOptionDescription method [Internationalization for Windows Applications],ISpellChecker interface, ISpellChecker interface [Internationalization for Windows Applications],GetOptionDescription method, ISpellChecker.GetOptionDescription, ISpellChecker::GetOptionDescription, intl.ispellchecker_getoptiondescription, spellcheck/ISpellChecker::GetOptionDescription
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
 - ISpellChecker::GetOptionDescription
 - spellcheck/ISpellChecker::GetOptionDescription
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
 - ISpellChecker.GetOptionDescription
---

# ISpellChecker::GetOptionDescription


## -description

Retrieves the information (id, description, heading and labels) of a specific option.

## -parameters

### -param optionId [in]

Identifier of the option to be retrieved.

### -param value [out, retval]

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ioptiondescription">IOptionDescription</a> interface that contains the information about <i>optionId</i>.

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

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ioptiondescription">IOptionDescription</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>
