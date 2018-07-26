---
UID: NF:spellcheck.ISpellChecker.add_SpellCheckerChanged
title: ISpellChecker::add_SpellCheckerChanged
author: windows-sdk-content
description: Adds an event handler (ISpellCheckerChangedEventHandler) for the SpellCheckerChanged event.
old-location: intl\ispellchecker_add_spellcheckerchanged.htm
old-project: Intl
ms.assetid: d539ab54-8a09-4857-8b48-5d19a34a5865
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: ISpellChecker interface [Internationalization for Windows Applications],add_SpellCheckerChanged method, ISpellChecker.add_SpellCheckerChanged, ISpellChecker::add_SpellCheckerChanged, add_SpellCheckerChanged, add_SpellCheckerChanged method [Internationalization for Windows Applications], add_SpellCheckerChanged method [Internationalization for Windows Applications],ISpellChecker interface, intl.ispellchecker_add_spellcheckerchanged, spellcheck/ISpellChecker::add_SpellCheckerChanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WORDLIST_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheck.h
api_name:
 - ISpellChecker.add_SpellCheckerChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellChecker::add_SpellCheckerChanged


## -description


Adds an event handler (<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>) for the SpellCheckerChanged event.


## -parameters




### -param handler [in]

The handler to invoke when the spell checker changes.


### -param eventCookie [out, retval]

An event cookie that uniquely identifies the added handler. This cookie must be passed to <a href="https://msdn.microsoft.com/66f62590-2d86-4747-a9e8-ea02f26eeb4d">remove_SpellCheckerChanged</a> to stop this handler from being invoked by spell checker changes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The SpellCheckerChanged event fires whenever the state of the spell checker changes in a way such that any text that has been checked should be rechecked. This should happen when the contents of a word list changes, when an option changes, or when the default spell checker changes.




## -see-also




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>



<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>



<a href="https://msdn.microsoft.com/66f62590-2d86-4747-a9e8-ea02f26eeb4d">remove_SpellCheckerChanged</a>
 

 

