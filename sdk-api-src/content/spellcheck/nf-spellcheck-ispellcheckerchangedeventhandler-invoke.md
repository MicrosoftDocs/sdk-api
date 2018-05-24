---
UID: NF:spellcheck.ISpellCheckerChangedEventHandler.Invoke
title: ISpellCheckerChangedEventHandler::Invoke
author: windows-driver-content
description: Receives the SpellCheckerChanged event.
old-location: intl\ispellcheckerchangedeventhandler_invoke.htm
old-project: Intl
ms.assetid: 585f147f-b644-4b6a-81d6-8ffeeb39d76a
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: ISpellCheckerChangedEventHandler interface [Internationalization for Windows Applications],Invoke method, ISpellCheckerChangedEventHandler.Invoke, ISpellCheckerChangedEventHandler::Invoke, Invoke, Invoke method [Internationalization for Windows Applications], Invoke method [Internationalization for Windows Applications],ISpellCheckerChangedEventHandler interface, intl.ispellcheckerchangedeventhandler_invoke, spellcheck/ISpellCheckerChangedEventHandler::Invoke
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheck.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WORDLIST_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Spellcheck.h
api_name:
-	ISpellCheckerChangedEventHandler.Invoke
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellCheckerChangedEventHandler::Invoke


## -description


Receives the SpellCheckerChanged event.


## -parameters




### -param sender [in]

The <a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a> that fired the event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called when there is a change to the state of the spell checker that could cause text to be treated differently. A client should recheck the text when this event is received.




## -see-also




<a href="https://msdn.microsoft.com/3cc5f675-048d-4ef3-9b66-5f081ee17a18">ISpellChecker</a>



<a href="https://msdn.microsoft.com/9dd1f768-a901-4682-9530-019fe1dfbf0b">ISpellCheckerChangedEventHandler</a>
 

 

