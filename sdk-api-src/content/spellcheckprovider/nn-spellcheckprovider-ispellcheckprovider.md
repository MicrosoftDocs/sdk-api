---
UID: NN:spellcheckprovider.ISpellCheckProvider
title: ISpellCheckProvider (spellcheckprovider.h)
author: windows-sdk-content
description: Represents a particular spell checker provider for a particular language, to be used by the spell checking infrastructure.
old-location: intl\ispellcheckprovider.htm
tech.root: Intl
ms.assetid: D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpellCheckProvider, ISpellCheckProvider interface [Internationalization for Windows Applications], ISpellCheckProvider interface [Internationalization for Windows Applications],described, intl.ispellcheckprovider, spellcheckprovider/ISpellCheckProvider
ms.topic: interface
f1_keywords: 
 - "spellcheckprovider/ISpellCheckProvider"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheckprovider.h
api_name:
 - ISpellCheckProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpellCheckProvider interface


## -description


Represents a particular spell checker provider for a particular language, to be used by the spell checking infrastructure.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpellCheckProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISpellCheckProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check">Check</a>
</td>
<td align="left" width="63%">
Checks the spelling of the supplied text and returns a collection of spelling errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-getoptiondescription">GetOptionDescription</a>
</td>
<td align="left" width="63%">
Retrieves the information (id, description, heading and labels) of a specific option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-getoptionvalue">GetOptionValue</a>
</td>
<td align="left" width="63%">
Retrieves the value associated with the given option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-initializewordlist">InitializeWordlist</a>
</td>
<td align="left" width="63%">
Initialize the specified word list to contain only the specified words.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-setoptionvalue">SetOptionValue</a>
</td>
<td align="left" width="63%">
Sets the value associated with the given option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-suggest">Suggest</a>
</td>
<td align="left" width="63%">
Retrieves spelling suggestions for the supplied text.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-get_id">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the identifier for this spell checker engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-get_languagetag">LanguageTag</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-get_localizedname">LocalizedName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-get_optionids">OptionIds</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets all of the declared option identifiers recognized by the spell checker.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckproviderfactory">ISpellCheckProviderFactory</a>
 

 

