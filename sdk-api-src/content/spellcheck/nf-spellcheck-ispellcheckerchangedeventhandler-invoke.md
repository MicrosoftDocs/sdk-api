---
UID: NF:spellcheck.ISpellCheckerChangedEventHandler.Invoke
title: ISpellCheckerChangedEventHandler::Invoke (spellcheck.h)
author: windows-sdk-content
description: Receives the SpellCheckerChanged event.
old-location: intl\ispellcheckerchangedeventhandler_invoke.htm
tech.root: Intl
ms.assetid: 585f147f-b644-4b6a-81d6-8ffeeb39d76a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpellCheckerChangedEventHandler interface [Internationalization for Windows Applications],Invoke method, ISpellCheckerChangedEventHandler.Invoke, ISpellCheckerChangedEventHandler::Invoke, Invoke, Invoke method [Internationalization for Windows Applications], Invoke method [Internationalization for Windows Applications],ISpellCheckerChangedEventHandler interface, intl.ispellcheckerchangedeventhandler_invoke, spellcheck/ISpellCheckerChangedEventHandler::Invoke
ms.topic: method
f1_keywords: 
 - "spellcheck/ISpellCheckerChangedEventHandler.Invoke"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheck.h
api_name:
 - ISpellCheckerChangedEventHandler.Invoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpellCheckerChangedEventHandler::Invoke


## -description


Receives the SpellCheckerChanged event.


## -parameters




### -param sender [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a> that fired the event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called when there is a change to the state of the spell checker that could cause text to be treated differently. A client should recheck the text when this event is received.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerchangedeventhandler">ISpellCheckerChangedEventHandler</a>
 

 

