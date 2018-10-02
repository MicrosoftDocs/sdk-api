---
UID: NN:spellcheckprovider.ISpellCheckProvider
title: ISpellCheckProvider
author: windows-sdk-content
description: Represents a particular spell checker provider for a particular language, to be used by the spell checking infrastructure.
old-location: intl\ispellcheckprovider.htm
tech.root: Intl
ms.assetid: D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ISpellCheckProvider, ISpellCheckProvider interface [Internationalization for Windows Applications], ISpellCheckProvider interface [Internationalization for Windows Applications],described, intl.ispellcheckprovider, spellcheckprovider/ISpellCheckProvider
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
---

# ISpellCheckProvider interface


## -description


Represents a particular spell checker provider for a particular language, to be used by the spell checking infrastructure.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpellCheckProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/B8C62B56-FF72-4C94-AC77-A6BEFCFE2589">Check</a>
</td>
<td align="left" width="63%">
Checks the spelling of the supplied text and returns a collection of spelling errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0F2ED4B7-AE71-4431-83FE-739F7D0D5CD2">GetOptionDescription</a>
</td>
<td align="left" width="63%">
Retrieves the information (id, description, heading and labels) of a specific option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4EE5DE54-DCA2-4DDC-BDE1-6417E4ADF4A2">GetOptionValue</a>
</td>
<td align="left" width="63%">
Retrieves the value associated with the given option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B1E3D0F9-8A6B-431F-A8AF-46D783E23FEF">InitializeWordlist</a>
</td>
<td align="left" width="63%">
Initialize the specified word list to contain only the specified words.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/635E6024-DD9F-403D-B05F-B719EFE78FC0">SetOptionValue</a>
</td>
<td align="left" width="63%">
Sets the value associated with the given option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4A66619C-8A12-4465-889C-B880C43031AB">Suggest</a>
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

<a href="https://msdn.microsoft.com/4FB41CF0-1F08-42F8-86A7-F38FE740F436">Id</a>


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

<a href="https://msdn.microsoft.com/74ED381D-3BF5-4E43-85DA-8CD53C821979">LanguageTag</a>


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

<a href="https://msdn.microsoft.com/05776188-1299-40BC-AD53-88DD01B65331">LocalizedName</a>


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

<a href="https://msdn.microsoft.com/E776D178-D5F0-4761-8A0C-7108C36AE3B1">OptionIds</a>


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




<a href="https://msdn.microsoft.com/680EC2D1-740E-40A8-9721-AC53AF17AC09">ISpellCheckProviderFactory</a>
 

 

