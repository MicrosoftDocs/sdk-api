---
UID: NN:spellcheck.ISpellChecker
title: ISpellChecker (spellcheck.h)
author: windows-sdk-content
description: Represents a particular spell checker for a particular language.
old-location: intl\ispellchecker.htm
tech.root: Intl
ms.assetid: 3cc5f675-048d-4ef3-9b66-5f081ee17a18
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpellChecker, ISpellChecker interface [Internationalization for Windows Applications], ISpellChecker interface [Internationalization for Windows Applications],described, intl.ispellchecker, spellcheck/ISpellChecker
ms.topic: interface
f1_keywords: 
 - "spellcheck/ISpellChecker"
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
 - ISpellChecker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpellChecker interface


## -description


Represents a particular spell checker for a particular language.

The <b>ISpellChecker</b> can be used to check text, get suggestions, update user dictionaries, and maintain options.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellChecker</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpellChecker</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add">Add</a>
</td>
<td align="left" width="63%">
Treats the provided word as though it were part of the original dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add_spellcheckerchanged">add_SpellCheckerChanged</a>
</td>
<td align="left" width="63%">
Adds an event handler (<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerchangedeventhandler">ISpellCheckerChangedEventHandler</a>) for the SpellCheckerChanged event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-autocorrect">AutoCorrect</a>
</td>
<td align="left" width="63%">
Causes occurrences of one word to be replaced by another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-check">Check</a>
</td>
<td align="left" width="63%">
Checks the spelling of the supplied text and returns a collection of spelling errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck">ComprehensiveCheck</a>
</td>
<td align="left" width="63%">
Checks the spelling of the supplied text in a more thorough manner than <a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-check">ISpellChecker::Check</a>, and returns a collection of spelling errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-getoptiondescription">GetOptionDescription</a>
</td>
<td align="left" width="63%">
Retrieves the information (id, description, heading and labels) of a specific option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-getoptionvalue">GetOptionValue</a>
</td>
<td align="left" width="63%">
Retrieves the value associated with the given option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-ignore">Ignore</a>
</td>
<td align="left" width="63%">
Ignores the provided word for the rest of this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-remove_spellcheckerchanged">remove_SpellCheckerChanged</a>
</td>
<td align="left" width="63%">
Removes an event handler (<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerchangedeventhandler">ISpellCheckerChangedEventHandler</a>) that has been added for the SpellCheckerChanged event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-suggest">Suggest</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-get_id">Id</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-get_languagetag">LanguageTag</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-get_localizedname">LocalizedName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-get_optionids">OptionIds</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets all of the declared option identifiers.

</td>
</tr>
</table> 

