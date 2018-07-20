---
UID: NF:spellcheck.ISpellCheckerFactory.get_SupportedLanguages
title: ISpellCheckerFactory::get_SupportedLanguages
author: windows-sdk-content
description: Gets the set of languages/dialects supported by any of the registered spell checkers.
old-location: intl\ispellcheckerfactory_supportedlanguages.htm
old-project: Intl
ms.assetid: ae6794fd-ce7c-4c62-abc5-824699054a37
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ISpellCheckerFactory interface [Internationalization for Windows Applications],SupportedLanguages property, ISpellCheckerFactory.SupportedLanguages, ISpellCheckerFactory.get_SupportedLanguages, ISpellCheckerFactory::SupportedLanguages, ISpellCheckerFactory::get_SupportedLanguages, SupportedLanguages property [Internationalization for Windows Applications], SupportedLanguages property [Internationalization for Windows Applications],ISpellCheckerFactory interface, get_SupportedLanguages, intl.ispellcheckerfactory_supportedlanguages, spellcheck/ISpellCheckerFactory::SupportedLanguages, spellcheck/ISpellCheckerFactory::get_SupportedLanguages
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
 - ISpellCheckerFactory.SupportedLanguages
 - ISpellCheckerFactory.get_SupportedLanguages
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpellCheckerFactory::get_SupportedLanguages


## -description


Gets the set of languages/dialects supported by any of the registered spell checkers.

This property is read-only.


## -parameters


## -remarks



The supported languages are specific, not neutral. For Hebrew, for example, the supported language is "he-IL", not "he".




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=227302">BCP47 Tags for Identifying Languages</a>



<a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>



<a href="https://msdn.microsoft.com/7febbb7e-c557-4698-bf58-6e6e7f61b071">ISpellCheckerFactory</a>
 

 

