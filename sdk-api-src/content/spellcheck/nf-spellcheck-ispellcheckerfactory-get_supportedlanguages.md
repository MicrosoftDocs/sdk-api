---
UID: NF:spellcheck.ISpellCheckerFactory.get_SupportedLanguages
title: ISpellCheckerFactory::get_SupportedLanguages (spellcheck.h)
description: Gets the set of languages/dialects supported by any of the registered spell checkers.
helpviewer_keywords: ["ISpellCheckerFactory interface [Internationalization for Windows Applications]","SupportedLanguages property","ISpellCheckerFactory.SupportedLanguages","ISpellCheckerFactory.get_SupportedLanguages","ISpellCheckerFactory::SupportedLanguages","ISpellCheckerFactory::get_SupportedLanguages","SupportedLanguages property [Internationalization for Windows Applications]","SupportedLanguages property [Internationalization for Windows Applications]","ISpellCheckerFactory interface","get_SupportedLanguages","intl.ispellcheckerfactory_supportedlanguages","spellcheck/ISpellCheckerFactory::SupportedLanguages","spellcheck/ISpellCheckerFactory::get_SupportedLanguages"]
old-location: intl\ispellcheckerfactory_supportedlanguages.htm
tech.root: Intl
ms.assetid: ae6794fd-ce7c-4c62-abc5-824699054a37
ms.date: 12/05/2018
ms.keywords: ISpellCheckerFactory interface [Internationalization for Windows Applications],SupportedLanguages property, ISpellCheckerFactory.SupportedLanguages, ISpellCheckerFactory.get_SupportedLanguages, ISpellCheckerFactory::SupportedLanguages, ISpellCheckerFactory::get_SupportedLanguages, SupportedLanguages property [Internationalization for Windows Applications], SupportedLanguages property [Internationalization for Windows Applications],ISpellCheckerFactory interface, get_SupportedLanguages, intl.ispellcheckerfactory_supportedlanguages, spellcheck/ISpellCheckerFactory::SupportedLanguages, spellcheck/ISpellCheckerFactory::get_SupportedLanguages
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
 - ISpellCheckerFactory::get_SupportedLanguages
 - spellcheck/ISpellCheckerFactory::get_SupportedLanguages
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
 - ISpellCheckerFactory.SupportedLanguages
 - ISpellCheckerFactory.get_SupportedLanguages
---

# ISpellCheckerFactory::get_SupportedLanguages


## -description

Gets the set of languages/dialects supported by any of the registered spell checkers.

This property is read-only.

## -parameters

## -remarks

The supported languages are specific, not neutral. For Hebrew, for example, the supported language is "he-IL", not "he".

## -see-also

<a href="http://tools.ietf.org/html/bcp47">BCP47 Tags for Identifying Languages</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerfactory">ISpellCheckerFactory</a>