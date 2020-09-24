---
UID: NN:spellcheck.ISpellChecker2
title: ISpellChecker2 (spellcheck.h)
description: Represents a particular spell checker for a particular language, with the added ability to remove words from the added words dictionary, or from the ignore list.
helpviewer_keywords: ["ISpellChecker2","ISpellChecker2 interface [Internationalization for Windows Applications]","ISpellChecker2 interface [Internationalization for Windows Applications]","described","intl.ispellchecker2","spellcheck/ISpellChecker2"]
old-location: intl\ispellchecker2.htm
tech.root: Intl
ms.assetid: 615C52CD-BD4D-4AC0-9732-6AB6BD7A930F
ms.date: 12/05/2018
ms.keywords: ISpellChecker2, ISpellChecker2 interface [Internationalization for Windows Applications], ISpellChecker2 interface [Internationalization for Windows Applications],described, intl.ispellchecker2, spellcheck/ISpellChecker2
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ISpellChecker2
 - spellcheck/ISpellChecker2
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
 - ISpellChecker2
---

# ISpellChecker2 interface


## -description

Represents a particular spell checker for a particular language, with the added ability to remove words from the added words dictionary, or from the ignore list.

The <b>ISpellChecker2</b> can also be used to check text, get suggestions, update user dictionaries, and maintain options, as can <a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a> from which it is derived.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellChecker2</b> interface inherits from <a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>. <b>ISpellChecker2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpellChecker2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker2-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes a word that was previously added by <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add">ISpellChecker.Add</a>, or set by <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-ignore">ISpellChecker.Ignore</a> to be ignored.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>