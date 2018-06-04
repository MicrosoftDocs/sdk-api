---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/809d1a71-bb14-4516-9624-2f10fe19a5d9">IOptionDescription</a>
 

 

