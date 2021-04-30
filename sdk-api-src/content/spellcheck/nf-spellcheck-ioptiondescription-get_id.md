---
UID: NF:spellcheck.IOptionDescription.get_Id
title: IOptionDescription::get_Id (spellcheck.h)
description: Gets the identifier of the spell checker option.
old-location: intl\ioptiondescription_id.htm
tech.root: Intl
ms.assetid: 09dba873-4302-46ee-9de0-cd480a424144
ms.date: 12/05/2018
ms.keywords: IOptionDescription interface [Internationalization for Windows Applications],Id property, IOptionDescription.Id, IOptionDescription.get_Id, IOptionDescription::Id, IOptionDescription::get_Id, Id property [Internationalization for Windows Applications], Id property [Internationalization for Windows Applications],IOptionDescription interface, get_Id, intl.ioptiondescription_id, spellcheck/IOptionDescription::Id, spellcheck/IOptionDescription::get_Id
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOptionDescription::get_Id
 - spellcheck/IOptionDescription::get_Id
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
 - IOptionDescription.Id
 - IOptionDescription.get_Id
---

# IOptionDescription::get_Id


## -description

Gets the identifier of the spell checker option.

This property is read-only.

## -parameters

## -remarks

Option identifiers all exist in the same area. Spell checker providers should use the engine identifier and the language tag (if the option is language-specific) to disambiguate potential collisions. 

Specifically, the structure for naming the option identifiers should be:

<ul>
<li><b>For the Microsoft spell checker engine:</b> &lt;language tag&gt;:&lt;option name&gt;. For example, "pt-BR:2009Reform."</li>
<li><b>For spell check provider engines:</b> &lt;engine id&gt;:&lt;language tag&gt;:&lt;option name&gt; (the language tag may be omitted if the option is not language specific). For example, "samplespell:fr-FR:AccentedUppercase".</li>
</ul>
<div class="alert"><b>Note</b>  Spell check providers are allowed to support existing Microsoft option identifiers, but they must not create new option identifiers in the Microsoft namespace. That is, spell check providers must use the engine identifier as a prefix.</div>
<div> </div>
An option identifier is linked to the set of labels and the semantics associated with them. If any change needs to be made between versions to the option (adding a label to the set of labels), a new option with a new identifier must be used. The only valid change that does not require a new identifier is to change from a single label to two labels and vice-versa when the semantics for values 0 and 1 do not change.

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ioptiondescription">IOptionDescription</a>