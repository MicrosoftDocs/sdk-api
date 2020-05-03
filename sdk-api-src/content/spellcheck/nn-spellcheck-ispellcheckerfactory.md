---
UID: NN:spellcheck.ISpellCheckerFactory
title: ISpellCheckerFactory (spellcheck.h)
description: A factory for instantiating a spell checker (ISpellChecker) as well as providing functionality for determining which languages are supported.helpviewer_keywords: ["ISpellCheckerFactory","ISpellCheckerFactory interface [Internationalization for Windows Applications]","ISpellCheckerFactory interface [Internationalization for Windows Applications]","described","intl.ispellcheckerfactory","spellcheck/ISpellCheckerFactory"]
old-location: intl\ispellcheckerfactory.htm
tech.root: Intl
ms.assetid: 7febbb7e-c557-4698-bf58-6e6e7f61b071
ms.date: 12/05/2018
ms.keywords: ISpellCheckerFactory, ISpellCheckerFactory interface [Internationalization for Windows Applications], ISpellCheckerFactory interface [Internationalization for Windows Applications],described, intl.ispellcheckerfactory, spellcheck/ISpellCheckerFactory
f1_keywords:
- spellcheck/ISpellCheckerFactory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Spellcheck.h
api_name:
- ISpellCheckerFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpellCheckerFactory interface


## -description


A factory for instantiating a spell checker (<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>) as well as providing functionality for determining which languages are supported.

<b>ISpellCheckerFactory</b> is the starting point for clients of the <a href="https://docs.microsoft.com/windows/desktop/Intl/spell-checker-api">Spell Checking API</a>, which should be created as an in-proc COM Server as shown in the example below.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckerFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpellCheckerFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISpellCheckerFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellcheckerfactory-createspellchecker">CreateSpellChecker</a>
</td>
<td align="left" width="63%">
Creates a spell checker that supports the specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellcheckerfactory-issupported">IsSupported</a>
</td>
<td align="left" width="63%">
Determines if the specified language is supported by a registered spell checker.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckerFactory</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellcheckerfactory-get_supportedlanguages">SupportedLanguages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the set of languages/dialects supported by any of the registered spell checkers.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>
 

 

