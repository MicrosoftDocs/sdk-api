---
UID: NE:spellcheck.CORRECTIVE_ACTION
title: CORRECTIVE_ACTION (spellcheck.h)
author: windows-sdk-content
description: Identifies the type of corrective action to be taken for a spelling error.
old-location: intl\corrective_action.htm
tech.root: Intl
ms.assetid: 370CF89E-97BF-4AB5-8AD6-3B2DF08463E0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CORRECTIVE_ACTION, CORRECTIVE_ACTION enumeration [Internationalization for Windows Applications], CORRECTIVE_ACTION_DELETE, CORRECTIVE_ACTION_GET_SUGGESTIONS, CORRECTIVE_ACTION_NONE, CORRECTIVE_ACTION_REPLACE, intl.corrective_action, spellcheck/CORRECTIVE_ACTION, spellcheck/CORRECTIVE_ACTION_DELETE, spellcheck/CORRECTIVE_ACTION_GET_SUGGESTIONS, spellcheck/CORRECTIVE_ACTION_NONE, spellcheck/CORRECTIVE_ACTION_REPLACE
ms.topic: enum
f1_keywords: 
 - "spellcheck/CORRECTIVE_ACTION"
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - SpellCheck.h
api_name:
 - CORRECTIVE_ACTION
product: Windows
targetos: Windows
req.typenames: CORRECTIVE_ACTION
req.redist: 
ms.custom: 19H1
---

# CORRECTIVE_ACTION enumeration


## -description


Identifies the type of corrective action to be taken for a spelling error.


## -enum-fields




### -field CORRECTIVE_ACTION_NONE

There are no errors.


### -field CORRECTIVE_ACTION_GET_SUGGESTIONS

The user should be prompted with a list of suggestions as returned by <a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-suggest">ISpellChecker::Suggest</a>.


### -field CORRECTIVE_ACTION_REPLACE

Replace the indicated erroneous text with the text provided in the suggestion. The user does not need to be prompted.


### -field CORRECTIVE_ACTION_DELETE

The user should be prompted to delete the indicated erroneous text.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-suggest">ISpellChecker::Suggest</a>



<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nf-spellcheck-ispellingerror-get_correctiveaction">ISpellingError::CorrectiveAction</a>
 

 

