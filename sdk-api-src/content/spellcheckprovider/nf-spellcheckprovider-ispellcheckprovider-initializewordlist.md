---
UID: NF:spellcheckprovider.ISpellCheckProvider.InitializeWordlist
title: ISpellCheckProvider::InitializeWordlist (spellcheckprovider.h)
description: Initialize the specified word list to contain only the specified words.
helpviewer_keywords: ["ISpellCheckProvider interface [Internationalization for Windows Applications]","InitializeWordlist method","ISpellCheckProvider.InitializeWordlist","ISpellCheckProvider::InitializeWordlist","InitializeWordlist","InitializeWordlist method [Internationalization for Windows Applications]","InitializeWordlist method [Internationalization for Windows Applications]","ISpellCheckProvider interface","intl.ispellcheckprovider_initializewordlist","spellcheckprovider/ISpellCheckProvider::InitializeWordlist"]
old-location: intl\ispellcheckprovider_initializewordlist.htm
tech.root: Intl
ms.assetid: B1E3D0F9-8A6B-431F-A8AF-46D783E23FEF
ms.date: 12/05/2018
ms.keywords: ISpellCheckProvider interface [Internationalization for Windows Applications],InitializeWordlist method, ISpellCheckProvider.InitializeWordlist, ISpellCheckProvider::InitializeWordlist, InitializeWordlist, InitializeWordlist method [Internationalization for Windows Applications], InitializeWordlist method [Internationalization for Windows Applications],ISpellCheckProvider interface, intl.ispellcheckprovider_initializewordlist, spellcheckprovider/ISpellCheckProvider::InitializeWordlist
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
 - ISpellCheckProvider::InitializeWordlist
 - spellcheckprovider/ISpellCheckProvider::InitializeWordlist
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
 - ISpellCheckProvider.InitializeWordlist
---

# ISpellCheckProvider::InitializeWordlist


## -description

Initialize the specified word list to contain only the specified words.

## -parameters

### -param wordlistType [in]

The type of word list.

### -param words [in]

The set of words to be included in the word list, passed as an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> object..

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
<i>wordlistType</i> is not a valid member of the <a href="/windows/desktop/api/spellcheck/ne-spellcheck-wordlist_type">WORDLIST_TYPE</a> enumeration.

</td>
</tr>
</table>

## -remarks

This method is called by the system (for example, when the client calls <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add">ISpellChecker::Add</a>), which passes the words from the respective word list to the provider so that it can consider the word list when spell checking.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>



<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add">ISpellChecker::Add</a>



<a href="/windows/desktop/api/spellcheck/ne-spellcheck-wordlist_type">WORDLIST_TYPE</a>