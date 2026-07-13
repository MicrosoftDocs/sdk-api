---
UID: NN:spellcheck.ISpellCheckerFactory
title: ISpellCheckerFactory (spellcheck.h)
description: A factory for instantiating a spell checker (ISpellChecker) as well as providing functionality for determining which languages are supported.
helpviewer_keywords: ["ISpellCheckerFactory","ISpellCheckerFactory interface [Internationalization for Windows Applications]","ISpellCheckerFactory interface [Internationalization for Windows Applications]","described","intl.ispellcheckerfactory","spellcheck/ISpellCheckerFactory"]
old-location: intl\ispellcheckerfactory.htm
tech.root: Intl
ms.assetid: 7febbb7e-c557-4698-bf58-6e6e7f61b071
ms.date: 12/05/2018
ms.keywords: ISpellCheckerFactory, ISpellCheckerFactory interface [Internationalization for Windows Applications], ISpellCheckerFactory interface [Internationalization for Windows Applications],described, intl.ispellcheckerfactory, spellcheck/ISpellCheckerFactory
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
 - ISpellCheckerFactory
 - spellcheck/ISpellCheckerFactory
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
 - ISpellCheckerFactory
---

# ISpellCheckerFactory interface


## -description

A factory for instantiating a spell checker (<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>) as well as providing functionality for determining which languages are supported.

<b>ISpellCheckerFactory</b> is the starting point for clients of the <a href="/windows/desktop/Intl/spell-checker-api">Spell Checking API</a>, which should be created as an in-proc COM Server as shown in the example below.

## -inheritance

The <b>ISpellCheckerFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpellCheckerFactory</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellchecker">ISpellChecker</a>
