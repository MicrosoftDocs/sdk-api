---
UID: NF:spellcheck.ISpellingError.get_Replacement
title: ISpellingError::get_Replacement (spellcheck.h)
description: Gets the text to use as replacement text when the corrective action is replace.
helpviewer_keywords: ["ISpellingError interface [Internationalization for Windows Applications]","Replacement property","ISpellingError.Replacement","ISpellingError.get_Replacement","ISpellingError::Replacement","ISpellingError::get_Replacement","Replacement property [Internationalization for Windows Applications]","Replacement property [Internationalization for Windows Applications]","ISpellingError interface","get_Replacement","intl.ispellingerror_replacement","spellcheck/ISpellingError::Replacement","spellcheck/ISpellingError::get_Replacement"]
old-location: intl\ispellingerror_replacement.htm
tech.root: Intl
ms.assetid: df161212-8950-4d05-9f69-15165fea9da9
ms.date: 12/05/2018
ms.keywords: ISpellingError interface [Internationalization for Windows Applications],Replacement property, ISpellingError.Replacement, ISpellingError.get_Replacement, ISpellingError::Replacement, ISpellingError::get_Replacement, Replacement property [Internationalization for Windows Applications], Replacement property [Internationalization for Windows Applications],ISpellingError interface, get_Replacement, intl.ispellingerror_replacement, spellcheck/ISpellingError::Replacement, spellcheck/ISpellingError::get_Replacement
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
 - ISpellingError::get_Replacement
 - spellcheck/ISpellingError::get_Replacement
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
 - ISpellingError.Replacement
 - ISpellingError.get_Replacement
---

# ISpellingError::get_Replacement


## -description

Gets the text to use as replacement text when the corrective action is replace.

This property is read-only.

## -parameters

## -remarks

If the <a href="/windows/desktop/api/spellcheck/ne-spellcheck-corrective_action">CORRECTIVE_ACTION</a> returned by <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellingerror-get_correctiveaction">CorrectiveAction</a> is not <b>CORRECTIVE_ACTION_REPLACE</b>, <i>value</i> is the empty string.

## -see-also

<a href="/windows/desktop/api/spellcheck/ne-spellcheck-corrective_action">CORRECTIVE_ACTION</a>



<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellingerror-get_correctiveaction">CorrectiveAction</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellingerror">ISpellingError</a>