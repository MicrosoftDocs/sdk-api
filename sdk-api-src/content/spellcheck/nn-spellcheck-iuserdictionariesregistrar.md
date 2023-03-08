---
UID: NN:spellcheck.IUserDictionariesRegistrar
title: IUserDictionariesRegistrar (spellcheck.h)
description: Manages the registration of user dictionaries.
helpviewer_keywords: ["IUserDictionariesRegistrar","IUserDictionariesRegistrar interface [Internationalization for Windows Applications]","IUserDictionariesRegistrar interface [Internationalization for Windows Applications]","described","intl.iuserdictionariesregistrar","spellcheck/IUserDictionariesRegistrar"]
old-location: intl\iuserdictionariesregistrar.htm
tech.root: Intl
ms.assetid: eca9446a-268e-4318-a5e7-8bb8592c9660
ms.date: 12/05/2018
ms.keywords: IUserDictionariesRegistrar, IUserDictionariesRegistrar interface [Internationalization for Windows Applications], IUserDictionariesRegistrar interface [Internationalization for Windows Applications],described, intl.iuserdictionariesregistrar, spellcheck/IUserDictionariesRegistrar
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
 - IUserDictionariesRegistrar
 - spellcheck/IUserDictionariesRegistrar
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
 - IUserDictionariesRegistrar
---

# IUserDictionariesRegistrar interface


## -description

Manages the registration of user dictionaries.

## -inheritance

The <b>IUserDictionariesRegistrar</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUserDictionariesRegistrar</b> also has these types of members:

## -remarks

<b>IUserDictionariesRegistrar</b> allows clients to persistently register and unregister user dictionary files that exist in locations other than the usual dictionary path (<code>%AppData%\Microsoft\Spelling</code>). The dictionaries must have the same file formats as the ones located in the normal path and also should have the appropriate file extensions.
However, it is strongly recommended for clients to place their dictionaries under <code>%AppData%\Microsoft\Spelling</code> whenever possible—the spell checking functionality does not pick up changes in dictionaries outside that directory tree.

This interface is obtained through a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> in <a href="/windows/desktop/api/spellcheck/nn-spellcheck-ispellcheckerfactory">ISpellCheckerFactory</a>.

The combined size of all registered dictionary files must be less than 1 MB by default. This can be increased to 2 MB by setting the registry key HKEY_CURRENT_USER\Software\Microsoft\Spelling\Dictionaries\AllowBiggerUD to the value 1. For more information about the Windows registry, see <a href="/windows/desktop/SysInfo/registry">Registry</a>.
