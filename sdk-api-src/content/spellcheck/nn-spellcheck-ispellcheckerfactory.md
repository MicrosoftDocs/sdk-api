---
UID: NN:spellcheck.ISpellCheckerFactory
title: ISpellCheckerFactory
author: windows-sdk-content
description: A factory for instantiating a spell checker (ISpellChecker) as well as providing functionality for determining which languages are supported.
old-location: intl\ispellcheckerfactory.htm
tech.root: Intl
ms.assetid: 7febbb7e-c557-4698-bf58-6e6e7f61b071
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ISpellCheckerFactory, ISpellCheckerFactory interface [Internationalization for Windows Applications], ISpellCheckerFactory interface [Internationalization for Windows Applications],described, intl.ispellcheckerfactory, spellcheck/ISpellCheckerFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckerFactory interface


## -description


A factory for instantiating a spell checker (<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>) as well as providing functionality for determining which languages are supported.

<b>ISpellCheckerFactory</b> is the starting point for clients of the <a href="https://msdn.microsoft.com/4EE858FA-DD9B-487B-87A7-4D94C7E8C237">Spell Checking API</a>, which should be created as an in-proc COM Server as shown in the example below.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckerFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpellCheckerFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9167b675-01ec-4173-a790-5452907b5598">CreateSpellChecker</a>
</td>
<td align="left" width="63%">
Creates a spell checker that supports the specified language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb21850d-d490-4055-8910-70f9c0090f59">IsSupported</a>
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

<a href="https://msdn.microsoft.com/ae6794fd-ce7c-4c62-abc5-824699054a37">SupportedLanguages</a>


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




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>
 

 

