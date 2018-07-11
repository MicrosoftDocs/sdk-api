---
UID: NN:spellcheck.ISpellChecker
title: ISpellChecker
author: windows-sdk-content
description: Represents a particular spell checker for a particular language.
old-location: intl\ispellchecker.htm
old-project: Intl
ms.assetid: 3cc5f675-048d-4ef3-9b66-5f081ee17a18
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ISpellChecker, ISpellChecker interface [Internationalization for Windows Applications], ISpellChecker interface [Internationalization for Windows Applications],described, intl.ispellchecker, spellcheck/ISpellChecker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheck.idl
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
 - Spellcheck.h
api_name:
 - ISpellChecker
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellChecker interface


## -description


Represents a particular spell checker for a particular language.

The <b>ISpellChecker</b> can be used to check text, get suggestions, update user dictionaries, and maintain options.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellChecker</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpellChecker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISpellChecker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Treats the provided word as though it were part of the original dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d539ab54-8a09-4857-8b48-5d19a34a5865">add_SpellCheckerChanged</a>
</td>
<td align="left" width="63%">
Adds an event handler (<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>) for the SpellCheckerChanged event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c0d24dc-cec2-4304-bfbc-096fa4d0e8d0">AutoCorrect</a>
</td>
<td align="left" width="63%">
Causes occurrences of one word to be replaced by another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/687d7e2f-13b1-4871-8850-2b179a6ce786">Check</a>
</td>
<td align="left" width="63%">
Checks the spelling of the supplied text and returns a collection of spelling errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E364F423-AF17-4F91-993B-CEA0E50CAF67">ComprehensiveCheck</a>
</td>
<td align="left" width="63%">
Checks the spelling of the supplied text in a more thorough manner than <a href="https://msdn.microsoft.com/687d7e2f-13b1-4871-8850-2b179a6ce786">ISpellChecker::Check</a>, and returns a collection of spelling errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5947f6ee-ad52-4d4d-a013-0c7dced273c3">GetOptionDescription</a>
</td>
<td align="left" width="63%">
Retrieves the information (id, description, heading and labels) of a specific option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdbf4fa6-9827-40d5-81c0-008e166c9390">GetOptionValue</a>
</td>
<td align="left" width="63%">
Retrieves the value associated with the given option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e82dd7a3-3ec4-4ef4-a19f-ad44866bbb1c">Ignore</a>
</td>
<td align="left" width="63%">
Ignores the provided word for the rest of this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66f62590-2d86-4747-a9e8-ea02f26eeb4d">remove_SpellCheckerChanged</a>
</td>
<td align="left" width="63%">
Removes an event handler (<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>) that has been added for the SpellCheckerChanged event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd6b1d90-8dc0-4640-a43a-678b43e55cb5">Suggest</a>
</td>
<td align="left" width="63%">
Retrieves spelling suggestions for the supplied text.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellChecker</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the identifier for this spell checker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1765a0ec-798c-4d0f-af05-d4d028c71dda">LanguageTag</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <a href="http://go.microsoft.com/fwlink/p/?linkid=227302">BCP47</a> language tag this instance of the spell checker supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93bd9224-11fc-42cd-8b2a-93eec972a943">LocalizedName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets text, suitable to display to the user, that describes this spell checker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6770acd9-5dc7-4f86-a780-e724646a3d56">OptionIds</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets all of the declared option identifiers.

</td>
</tr>
</table> 

