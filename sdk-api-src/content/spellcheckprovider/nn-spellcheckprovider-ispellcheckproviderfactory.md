---
UID: NN:spellcheckprovider.ISpellCheckProviderFactory
title: ISpellCheckProviderFactory
author: windows-sdk-content
description: A factory for instantiating a spell checker (ISpellCheckProvider) as well as providing functionality for determining which languages are supported.
old-location: intl\ispellcheckproviderfactory.htm
old-project: Intl
ms.assetid: 680EC2D1-740E-40A8-9721-AC53AF17AC09
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISpellCheckProviderFactory, ISpellCheckProviderFactory interface [Internationalization for Windows Applications], ISpellCheckProviderFactory interface [Internationalization for Windows Applications],described, intl.ispellcheckproviderfactory, spellcheckprovider/ISpellCheckProviderFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WORDLIST_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheckprovider.h
api_name:
 - ISpellCheckProviderFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISpellCheckProviderFactory interface


## -description


A factory for instantiating a spell checker (<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>) as well as providing functionality for determining which languages are supported.

  This is instantiated by providers and used by the Spell Checking API.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckProviderFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpellCheckProviderFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E56E13D5-A41D-41F4-8E63-55664F6A8E28">CreateSpellCheckProvider</a>
</td>
<td align="left" width="63%">
Creates a spell checker (implemented by a spell check provider) that supports the specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88689384-E95E-4D56-BAD4-9889816F76EB">IsSupported</a>
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

<a href="https://msdn.microsoft.com/52690D99-4E14-44CE-BFD8-D0931F250280">SupportedLanguages</a>


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




<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>
 

 

