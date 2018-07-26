---
UID: NF:spellcheck.ISpellChecker.remove_SpellCheckerChanged
title: ISpellChecker::remove_SpellCheckerChanged
author: windows-sdk-content
description: Removes an event handler (ISpellCheckerChangedEventHandler) that has been added for the SpellCheckerChanged event.
old-location: intl\ispellchecker_remove_spellcheckerchanged.htm
old-project: Intl
ms.assetid: 66f62590-2d86-4747-a9e8-ea02f26eeb4d
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: ISpellChecker interface [Internationalization for Windows Applications],remove_SpellCheckerChanged method, ISpellChecker.remove_SpellCheckerChanged, ISpellChecker::remove_SpellCheckerChanged, intl.ispellchecker_remove_spellcheckerchanged, remove_SpellCheckerChanged, remove_SpellCheckerChanged method [Internationalization for Windows Applications], remove_SpellCheckerChanged method [Internationalization for Windows Applications],ISpellChecker interface, spellcheck/ISpellChecker::remove_SpellCheckerChanged
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
 - ISpellChecker.remove_SpellCheckerChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellChecker::remove_SpellCheckerChanged


## -description


Removes an event handler (<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>) that has been added for the SpellCheckerChanged event.


## -parameters




### -param eventCookie [in]

The event cookie that uniquely identifies the added handler. This is the <i>eventCookie</i> that was obtained from the call to <a href="https://msdn.microsoft.com/d539ab54-8a09-4857-8b48-5d19a34a5865">add_SpellCheckerChanged</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>



<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>



<a href="https://msdn.microsoft.com/d539ab54-8a09-4857-8b48-5d19a34a5865">add_SpellCheckerChanged</a>
 

 

