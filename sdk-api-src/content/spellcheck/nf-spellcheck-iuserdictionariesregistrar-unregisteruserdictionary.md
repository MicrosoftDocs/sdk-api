---
UID: NF:spellcheck.IUserDictionariesRegistrar.UnregisterUserDictionary
title: IUserDictionariesRegistrar::UnregisterUserDictionary (spellcheck.h)
description: Unregisters a previously registered user dictionary.
helpviewer_keywords: ["IUserDictionariesRegistrar interface [Internationalization for Windows Applications]","UnregisterUserDictionary method","IUserDictionariesRegistrar.UnregisterUserDictionary","IUserDictionariesRegistrar::UnregisterUserDictionary","UnregisterUserDictionary","UnregisterUserDictionary method [Internationalization for Windows Applications]","UnregisterUserDictionary method [Internationalization for Windows Applications]","IUserDictionariesRegistrar interface","intl.iuserdictionariesregistrar_unregisteruserdictionary","spellcheck/IUserDictionariesRegistrar::UnregisterUserDictionary"]
old-location: intl\iuserdictionariesregistrar_unregisteruserdictionary.htm
tech.root: Intl
ms.assetid: 6b1756f5-7ab5-4408-896d-5ea5ae671651
ms.date: 12/05/2018
ms.keywords: IUserDictionariesRegistrar interface [Internationalization for Windows Applications],UnregisterUserDictionary method, IUserDictionariesRegistrar.UnregisterUserDictionary, IUserDictionariesRegistrar::UnregisterUserDictionary, UnregisterUserDictionary, UnregisterUserDictionary method [Internationalization for Windows Applications], UnregisterUserDictionary method [Internationalization for Windows Applications],IUserDictionariesRegistrar interface, intl.iuserdictionariesregistrar_unregisteruserdictionary, spellcheck/IUserDictionariesRegistrar::UnregisterUserDictionary
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
 - IUserDictionariesRegistrar::UnregisterUserDictionary
 - spellcheck/IUserDictionariesRegistrar::UnregisterUserDictionary
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
 - IUserDictionariesRegistrar.UnregisterUserDictionary
---

# IUserDictionariesRegistrar::UnregisterUserDictionary


## -description

Unregisters a previously registered user dictionary. The dictionary will no longer be used by the spell checking functionality.

## -parameters

### -param dictionaryPath [in]

The path of the dictionary file to be unregistered.

### -param languageTag [in]

The language for which this dictionary was used. It must match the language passed to <a href="/windows/desktop/api/spellcheck/nf-spellcheck-iuserdictionariesregistrar-registeruserdictionary">RegisterUserDictionary</a>.

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
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<i>dictionaryPath</i> or <i>languageTag</i> is a null pointer.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  To unregister a given file, this method must be passed the same arguments that were previously used to register it.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/spellcheck/nn-spellcheck-iuserdictionariesregistrar">IUserDictionariesRegistrar</a>