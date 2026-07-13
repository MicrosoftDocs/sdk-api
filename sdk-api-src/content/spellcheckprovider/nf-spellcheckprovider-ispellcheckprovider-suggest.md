---
UID: NF:spellcheckprovider.ISpellCheckProvider.Suggest
title: ISpellCheckProvider::Suggest (spellcheckprovider.h)
description: Retrieves spelling suggestions for the supplied text. (ISpellCheckProvider.Suggest)
helpviewer_keywords: ["ISpellCheckProvider interface [Internationalization for Windows Applications]","Suggest method","ISpellCheckProvider.Suggest","ISpellCheckProvider::Suggest","Suggest","Suggest method [Internationalization for Windows Applications]","Suggest method [Internationalization for Windows Applications]","ISpellCheckProvider interface","intl.ispellcheckprovider_suggest","spellcheckprovider/ISpellCheckProvider::Suggest"]
old-location: intl\ispellcheckprovider_suggest.htm
tech.root: Intl
ms.assetid: 4A66619C-8A12-4465-889C-B880C43031AB
ms.date: 12/05/2018
ms.keywords: ISpellCheckProvider interface [Internationalization for Windows Applications],Suggest method, ISpellCheckProvider.Suggest, ISpellCheckProvider::Suggest, Suggest, Suggest method [Internationalization for Windows Applications], Suggest method [Internationalization for Windows Applications],ISpellCheckProvider interface, intl.ispellcheckprovider_suggest, spellcheckprovider/ISpellCheckProvider::Suggest
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
 - ISpellCheckProvider::Suggest
 - spellcheckprovider/ISpellCheckProvider::Suggest
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
 - ISpellCheckProvider.Suggest
---

# ISpellCheckProvider::Suggest


## -description

Retrieves spelling suggestions for the supplied text.

## -parameters

### -param word [in]

The word or phrase to get suggestions for.

### -param value [out, retval]

The list of suggestions, returned as an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> object.

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
<i>word</i> is correctly spelled. <i>value</i> contains one entry, which is the text that was passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>word</i> is a null pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>
