---
UID: NF:spellcheckprovider.ISpellCheckProviderFactory.get_SupportedLanguages
title: ISpellCheckProviderFactory::get_SupportedLanguages (spellcheckprovider.h)
description: Gets the set of languages/dialects supported by the spell checker.
helpviewer_keywords: ["ISpellCheckProviderFactory interface [Internationalization for Windows Applications]","SupportedLanguages property","ISpellCheckProviderFactory.SupportedLanguages","ISpellCheckProviderFactory.get_SupportedLanguages","ISpellCheckProviderFactory::SupportedLanguages","ISpellCheckProviderFactory::get_SupportedLanguages","SupportedLanguages property [Internationalization for Windows Applications]","SupportedLanguages property [Internationalization for Windows Applications]","ISpellCheckProviderFactory interface","get_SupportedLanguages","intl.ispellcheckproviderfactory_supportedlanguages","spellcheckprovider/ISpellCheckProviderFactory::SupportedLanguages","spellcheckprovider/ISpellCheckProviderFactory::get_SupportedLanguages"]
old-location: intl\ispellcheckproviderfactory_supportedlanguages.htm
tech.root: Intl
ms.assetid: 52690D99-4E14-44CE-BFD8-D0931F250280
ms.date: 12/05/2018
ms.keywords: ISpellCheckProviderFactory interface [Internationalization for Windows Applications],SupportedLanguages property, ISpellCheckProviderFactory.SupportedLanguages, ISpellCheckProviderFactory.get_SupportedLanguages, ISpellCheckProviderFactory::SupportedLanguages, ISpellCheckProviderFactory::get_SupportedLanguages, SupportedLanguages property [Internationalization for Windows Applications], SupportedLanguages property [Internationalization for Windows Applications],ISpellCheckProviderFactory interface, get_SupportedLanguages, intl.ispellcheckproviderfactory_supportedlanguages, spellcheckprovider/ISpellCheckProviderFactory::SupportedLanguages, spellcheckprovider/ISpellCheckProviderFactory::get_SupportedLanguages
req.header: spellcheckprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheckprovider.idl
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
 - ISpellCheckProviderFactory::get_SupportedLanguages
 - spellcheckprovider/ISpellCheckProviderFactory::get_SupportedLanguages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheckprovider.h
api_name:
 - ISpellCheckProviderFactory.SupportedLanguages
 - ISpellCheckProviderFactory.get_SupportedLanguages
---

# ISpellCheckProviderFactory::get_SupportedLanguages


## -description

Gets the set of languages/dialects supported by the spell checker.

This property is read-only.

## -parameters

## -remarks

The supported languages are specific, not neutral. For Hebrew, for example, the supported language is "he-IL", not "he".

## -see-also

<a href="http://tools.ietf.org/html/bcp47">BCP47 Tags for Identifying Languages</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>



<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckproviderfactory">ISpellCheckProviderFactory</a>