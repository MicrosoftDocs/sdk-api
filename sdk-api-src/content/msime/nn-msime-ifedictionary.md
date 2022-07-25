---
UID: NN:msime.IFEDictionary
title: IFEDictionary (msime.h)
description: The IFEDictionary interface allows clients to access a Microsoft IME user dictionary.
helpviewer_keywords: ["IFEDictionary","IFEDictionary interface [Internationalization for Windows Applications]","IFEDictionary interface [Internationalization for Windows Applications]","described","intl.ifedictionary","msime/IFEDictionary"]
old-location: intl\ifedictionary.htm
tech.root: Intl
ms.assetid: 4C63FF43-0170-4038-AB01-72441E1BB189
ms.date: 12/05/2018
ms.keywords: IFEDictionary, IFEDictionary interface [Internationalization for Windows Applications], IFEDictionary interface [Internationalization for Windows Applications],described, intl.ifedictionary, msime/IFEDictionary
req.header: msime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IFEDictionary
 - msime/IFEDictionary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFEDictionary
---

# IFEDictionary interface


## -description

The <b>IFEDictionary</b> interface allows clients to access a Microsoft IME user dictionary.

This API enables your apps to access and use the data contained in the Microsoft IME dictionaries (including personal name and geographical name dictionaries), or user dictionary. You can develop and sell such applications, provided that:<ul>
<li>You do not create an application that accesses a dictionary that is not a Microsoft IME dictionary through this API.</li>
<li>You do not dump, copy, or distribute the dictionary data contained in the Microsoft IME.</li>
</ul>You must use this API only for the purpose of developing applications for users who already have the Microsoft IME.

## -inheritance

The <b>IFEDictionary</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFEDictionary</b> also has these types of members:

## -remarks

Create an instance of this interface with the <a href="/windows/desktop/api/msime/nf-msime-createifedictionaryinstance">CreateIFEDictionaryInstance</a> function.
