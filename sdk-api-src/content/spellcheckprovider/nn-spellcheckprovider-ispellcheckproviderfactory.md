---
UID: NN:spellcheckprovider.ISpellCheckProviderFactory
title: ISpellCheckProviderFactory (spellcheckprovider.h)
description: A factory for instantiating a spell checker (ISpellCheckProvider) as well as providing functionality for determining which languages are supported.
helpviewer_keywords: ["ISpellCheckProviderFactory","ISpellCheckProviderFactory interface [Internationalization for Windows Applications]","ISpellCheckProviderFactory interface [Internationalization for Windows Applications]","described","intl.ispellcheckproviderfactory","spellcheckprovider/ISpellCheckProviderFactory"]
old-location: intl\ispellcheckproviderfactory.htm
tech.root: Intl
ms.assetid: 680EC2D1-740E-40A8-9721-AC53AF17AC09
ms.date: 12/05/2018
ms.keywords: ISpellCheckProviderFactory, ISpellCheckProviderFactory interface [Internationalization for Windows Applications], ISpellCheckProviderFactory interface [Internationalization for Windows Applications],described, intl.ispellcheckproviderfactory, spellcheckprovider/ISpellCheckProviderFactory
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
 - ISpellCheckProviderFactory
 - spellcheckprovider/ISpellCheckProviderFactory
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
 - ISpellCheckProviderFactory
---

# ISpellCheckProviderFactory interface


## -description

A factory for instantiating a spell checker (<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>) as well as providing functionality for determining which languages are supported.

  This is instantiated by providers and used by the Spell Checking API.

## -inheritance

The <b>ISpellCheckProviderFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpellCheckProviderFactory</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider">ISpellCheckProvider</a>
