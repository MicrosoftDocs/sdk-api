---
UID: NF:spellcheck.ISpellChecker.add_SpellCheckerChanged
title: ISpellChecker::add_SpellCheckerChanged (spellcheck.h)
description: Adds an event handler (ISpellCheckerChangedEventHandler) for the SpellCheckerChanged event.
helpviewer_keywords: ["ISpellChecker interface [Internationalization for Windows Applications]","add_SpellCheckerChanged method","ISpellChecker.add_SpellCheckerChanged","ISpellChecker::add_SpellCheckerChanged","add_SpellCheckerChanged","add_SpellCheckerChanged method [Internationalization for Windows Applications]","add_SpellCheckerChanged method [Internationalization for Windows Applications]","ISpellChecker interface","intl.ispellchecker_add_spellcheckerchanged","spellcheck/ISpellChecker::add_SpellCheckerChanged"]
old-location: intl\ispellchecker_add_spellcheckerchanged.htm
tech.root: Intl
ms.assetid: d539ab54-8a09-4857-8b48-5d19a34a5865
ms.date: 12/05/2018
ms.keywords: ISpellChecker interface [Internationalization for Windows Applications],add_SpellCheckerChanged method, ISpellChecker.add_SpellCheckerChanged, ISpellChecker::add_SpellCheckerChanged, add_SpellCheckerChanged, add_SpellCheckerChanged method [Internationalization for Windows Applications], add_SpellCheckerChanged method [Internationalization for Windows Applications],ISpellChecker interface, intl.ispellchecker_add_spellcheckerchanged, spellcheck/ISpellChecker::add_SpellCheckerChanged
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
 - ISpellChecker::add_SpellCheckerChanged
 - spellcheck/ISpellChecker::add_SpellCheckerChanged
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
 - ISpellChecker.add_SpellCheckerChanged
---

# ISpellChecker::add_SpellCheckerChanged


## -description

Adds an event handler (<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerchangedeventhandler">ISpellCheckerChangedEventHandler</a>) for the SpellCheckerChanged event.

## -parameters

### -param handler [in]

The handler to invoke when the spell checker changes.

### -param eventCookie [out, retval]

An event cookie that uniquely identifies the added handler. This cookie must be passed to <a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-remove_spellcheckerchanged">remove_SpellCheckerChanged</a> to stop this handler from being invoked by spell checker changes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The SpellCheckerChanged event fires whenever the state of the spell checker changes in a way such that any text that has been checked should be rechecked. This should happen when the contents of a word list changes, when an option changes, or when the default spell checker changes.

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerchangedeventhandler">ISpellCheckerChangedEventHandler</a>



<a href="/windows/desktop/api/spellcheck/nf-spellcheck-ispellchecker-remove_spellcheckerchanged">remove_SpellCheckerChanged</a>