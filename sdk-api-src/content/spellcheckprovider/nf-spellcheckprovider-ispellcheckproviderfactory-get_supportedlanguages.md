---
UID: NF:spellcheckprovider.ISpellCheckProviderFactory.get_SupportedLanguages
title: ISpellCheckProviderFactory::get_SupportedLanguages
author: windows-sdk-content
description: Gets the set of languages/dialects supported by the spell checker.
old-location: intl\ispellcheckproviderfactory_supportedlanguages.htm
tech.root: Intl
ms.assetid: 52690D99-4E14-44CE-BFD8-D0931F250280
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISpellCheckProviderFactory interface [Internationalization for Windows Applications],SupportedLanguages property, ISpellCheckProviderFactory.SupportedLanguages, ISpellCheckProviderFactory.get_SupportedLanguages, ISpellCheckProviderFactory::SupportedLanguages, ISpellCheckProviderFactory::get_SupportedLanguages, SupportedLanguages property [Internationalization for Windows Applications], SupportedLanguages property [Internationalization for Windows Applications],ISpellCheckProviderFactory interface, get_SupportedLanguages, intl.ispellcheckproviderfactory_supportedlanguages, spellcheckprovider/ISpellCheckProviderFactory::SupportedLanguages, spellcheckprovider/ISpellCheckProviderFactory::get_SupportedLanguages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckProviderFactory::get_SupportedLanguages


## -description


Gets the set of languages/dialects supported by the spell checker.

This property is read-only.


## -parameters


## -remarks



The supported languages are specific, not neutral. For Hebrew, for example, the supported language is "he-IL", not "he".




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=227302">BCP47 Tags for Identifying Languages</a>



<a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>



<a href="https://msdn.microsoft.com/680EC2D1-740E-40A8-9721-AC53AF17AC09">ISpellCheckProviderFactory</a>
 

 

