---
UID: NE:spellcheck.WORDLIST_TYPE
title: WORDLIST_TYPE
author: windows-sdk-content
description: Identifies one of the types of word lists used by spell checkers.
old-location: intl\wordlist_type.htm
old-project: Intl
ms.assetid: F1D517F3-CAE3-46DC-867E-D8D73C20CF9A
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WORDLIST_TYPE, WORDLIST_TYPE enumeration [Internationalization for Windows Applications], WORDLIST_TYPE_ADD, WORDLIST_TYPE_AUTOCORRECT, WORDLIST_TYPE_EXCLUDE, WORDLIST_TYPE_IGNORE, intl.wordlist_type, spellcheck/WORDLIST_TYPE, spellcheck/WORDLIST_TYPE_ADD, spellcheck/WORDLIST_TYPE_AUTOCORRECT, spellcheck/WORDLIST_TYPE_EXCLUDE, spellcheck/WORDLIST_TYPE_IGNORE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: spellcheck.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SpatialInteractionManagerInterop.idl
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
 - HeaderDef
api_location:
 - SpellCheck.h
api_name:
 - WORDLIST_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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
 

 

