---
UID: NN:spellcheckprovider.ISpellCheckProviderFactory
title: ISpellCheckProviderFactory (spellcheckprovider.h)
description: A factory for instantiating a spell checker (ISpellCheckProvider) as well as providing functionality for determining which languages are supported.
helpviewer_keywords: ["ISpellCheckProviderFactory","ISpellCheckProviderFactory interface [Internationalization for Windows Applications]","ISpellCheckProviderFactory interface [Internationalization for Windows Applications]","described","intl.ispellcheckproviderfactory","spellcheckprovider/ISpellCheckProviderFactory"]
old-location: intl\ispellcheckproviderfactory.htm
tech.root: Intl
ms.assetid: 680EC2D1-740E-40A8-9721-AC53AF17AC09
ms.date: 12/05/2018
ms.keywords: ISpellCheckProviderFactory, ISpellCheckProviderFactory interface [Internationalization for Windows Applications], ISpellCheckProviderFactory interface [Internationalization for Windows Applications],described, intl.ispellcheckproviderfactory, spellcheckprovider/ISpellCheckProviderFactory
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
 - ISpellCheckProviderFactory
 - spellcheckprovider/ISpellCheckProviderFactory
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
 - ISpellCheckProviderFactory
---

# ISpellCheckProviderFactory interface


## -description

A factory for instantiating a spell checker (<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>) as well as providing functionality for determining which languages are supported.

  This is instantiated by providers and used by the Spell Checking API.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckProviderFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpellCheckProviderFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISpellCheckProviderFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckproviderfactory-createspellcheckprovider">CreateSpellCheckProvider</a>
</td>
<td align="left" width="63%">
Creates a spell checker (implemented by a spell check provider) that supports the specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckproviderfactory-issupported">IsSupported</a>
</td>
<td align="left" width="63%">
Determines if the specified language is supported by this spell checker.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckProviderFactory</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckproviderfactory-get_supportedlanguages">SupportedLanguages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the set of languages/dialects supported by the spell checker.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>