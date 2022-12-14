---
UID: NF:spellcheck.ISpellChecker.remove_SpellCheckerChanged
title: ISpellChecker::remove_SpellCheckerChanged (spellcheck.h)
description: Removes an event handler (ISpellCheckerChangedEventHandler) that has been added for the SpellCheckerChanged event.
helpviewer_keywords: ["ISpellChecker interface [Internationalization for Windows Applications]","remove_SpellCheckerChanged method","ISpellChecker.remove_SpellCheckerChanged","ISpellChecker::remove_SpellCheckerChanged","intl.ispellchecker_remove_spellcheckerchanged","remove_SpellCheckerChanged","remove_SpellCheckerChanged method [Internationalization for Windows Applications]","remove_SpellCheckerChanged method [Internationalization for Windows Applications]","ISpellChecker interface","spellcheck/ISpellChecker::remove_SpellCheckerChanged"]
old-location: intl\ispellchecker_remove_spellcheckerchanged.htm
tech.root: Intl
ms.assetid: 66f62590-2d86-4747-a9e8-ea02f26eeb4d
ms.date: 12/05/2018
ms.keywords: ISpellChecker interface [Internationalization for Windows Applications],remove_SpellCheckerChanged method, ISpellChecker.remove_SpellCheckerChanged, ISpellChecker::remove_SpellCheckerChanged, intl.ispellchecker_remove_spellcheckerchanged, remove_SpellCheckerChanged, remove_SpellCheckerChanged method [Internationalization for Windows Applications], remove_SpellCheckerChanged method [Internationalization for Windows Applications],ISpellChecker interface, spellcheck/ISpellChecker::remove_SpellCheckerChanged
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
 - ISpellChecker::remove_SpellCheckerChanged
 - spellcheck/ISpellChecker::remove_SpellCheckerChanged
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
 - ISpellChecker.remove_SpellCheckerChanged
---

# ISpellChecker::remove_SpellCheckerChanged


## -description

Removes an event handler (<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerchangedeventhandler">ISpellCheckerChangedEventHandler</a>) that has been added for the SpellCheckerChanged event.

## -parameters

### -param eventCookie [in]

The event cookie that uniquely identifies the added handler. This is the <i>eventCookie</i> that was obtained from the call to <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add_spellcheckerchanged">add_SpellCheckerChanged</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerchangedeventhandler">ISpellCheckerChangedEventHandler</a>



<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-add_spellcheckerchanged">add_SpellCheckerChanged</a>