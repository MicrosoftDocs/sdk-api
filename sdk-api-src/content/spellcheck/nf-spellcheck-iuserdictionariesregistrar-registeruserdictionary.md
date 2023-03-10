---
UID: NF:spellcheck.IUserDictionariesRegistrar.RegisterUserDictionary
title: IUserDictionariesRegistrar::RegisterUserDictionary (spellcheck.h)
description: Registers a file to be used as a user dictionary for the current user, until unregistered.
helpviewer_keywords: ["IUserDictionariesRegistrar interface [Internationalization for Windows Applications]","RegisterUserDictionary method","IUserDictionariesRegistrar.RegisterUserDictionary","IUserDictionariesRegistrar::RegisterUserDictionary","RegisterUserDictionary","RegisterUserDictionary method [Internationalization for Windows Applications]","RegisterUserDictionary method [Internationalization for Windows Applications]","IUserDictionariesRegistrar interface","intl.iuserdictionariesregistrar_registeruserdictionary","spellcheck/IUserDictionariesRegistrar::RegisterUserDictionary"]
old-location: intl\iuserdictionariesregistrar_registeruserdictionary.htm
tech.root: Intl
ms.assetid: 5dd64e20-af2d-4d84-9e66-01ac19f34212
ms.date: 12/05/2018
ms.keywords: IUserDictionariesRegistrar interface [Internationalization for Windows Applications],RegisterUserDictionary method, IUserDictionariesRegistrar.RegisterUserDictionary, IUserDictionariesRegistrar::RegisterUserDictionary, RegisterUserDictionary, RegisterUserDictionary method [Internationalization for Windows Applications], RegisterUserDictionary method [Internationalization for Windows Applications],IUserDictionariesRegistrar interface, intl.iuserdictionariesregistrar_registeruserdictionary, spellcheck/IUserDictionariesRegistrar::RegisterUserDictionary
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
 - IUserDictionariesRegistrar::RegisterUserDictionary
 - spellcheck/IUserDictionariesRegistrar::RegisterUserDictionary
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
 - IUserDictionariesRegistrar.RegisterUserDictionary
---

# IUserDictionariesRegistrar::RegisterUserDictionary


## -description

Registers a file to be used as a user dictionary for the current user, until unregistered.

## -parameters

### -param dictionaryPath [in]

The path of the dictionary file to be registered.

### -param languageTag [in]

The language for which this dictionary should be used. If left empty, it will be used for any language.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The file is already registered for the language.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
The file doesn’t exist or isn't valid, or it doesn't have a valid extension (.dic, .exc, or .acl)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<i>dictionaryPath</i> or <i>languageTag</i> is a null pointer.

</td>
</tr>
</table>

## -remarks

The filename must have the extension .dic (added words), .exc (excluded words), or .acl (autocorrect word pairs). The files are  UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM). 
Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("|") (in the AutoCorrect word list). The wordlist in which the dictionary is included is inferred through the file extension.

A file registered for a language subtag will be picked up for all languages that contain it. For example, a dictionary registered for "en" will also be used by an "en-US" spell checker.

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-iuserdictionariesregistrar">IUserDictionariesRegistrar</a>