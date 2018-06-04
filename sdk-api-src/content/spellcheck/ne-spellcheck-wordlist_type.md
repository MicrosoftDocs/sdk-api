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

# WORDLIST_TYPE enumeration


## -description


Identifies one of the types of word lists used by spell checkers.


## -enum-fields




### -field WORDLIST_TYPE_IGNORE

Words considered to be correctly spelled, but which are not offered as  suggestions. This word list isn't saved and is specific to a spelling session. (The others types of word lists are saved in the default custom dictionary files, and are global.)


### -field WORDLIST_TYPE_ADD

Words considered to be correctly spelled and which can be offered as  suggestions.


### -field WORDLIST_TYPE_EXCLUDE

Words considered to be incorrectly spelled.


### -field WORDLIST_TYPE_AUTOCORRECT

Word pairs of a misspelled word and the word that should replace it.


## -remarks



Providers should consider the following priority order when doing spell checking:
Ignored Words &gt; AutoCorrected Words &gt; Excluded Words &gt; Added Words &gt; Spell checking algorithm.




## -see-also




<a href="https://msdn.microsoft.com/B1E3D0F9-8A6B-431F-A8AF-46D783E23FEF">ISpellCheckProvider::InitializeWordlist</a>
 

 

