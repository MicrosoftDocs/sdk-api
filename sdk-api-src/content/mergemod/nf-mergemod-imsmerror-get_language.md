---
UID: NF:mergemod.IMsmError.get_Language
title: IMsmError::get_Language (mergemod.h)
description: The get_Language method retrieves the Language property of the Error object. This function returns the LANGID of the error.
helpviewer_keywords: ["IMsmError interface","get_Language method","IMsmError.get_Language","IMsmError::get_Language","_msi_get_language_function_error_object_","get_Language","get_Language method","get_Language method","IMsmError interface","mergemod/IMsmError::get_Language","setup.imsmerror_get_language"]
old-location: setup\imsmerror_get_language.htm
tech.root: setup
ms.assetid: c0d14c18-facc-441c-89c6-85abe6d19443
ms.date: 12/05/2018
ms.keywords: IMsmError interface,get_Language method, IMsmError.get_Language, IMsmError::get_Language, _msi_get_language_function_error_object_, get_Language, get_Language method, get_Language method,IMsmError interface, mergemod/IMsmError::get_Language, setup.imsmerror_get_language
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.dll: Mergemod.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmError::get_Language
 - mergemod/IMsmError::get_Language
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmError.get_Language
---

# IMsmError::get_Language


## -description

The 
<b>get_Language</b> method retrieves the 
<a href="/windows/desktop/Msi/dependency-language">Language</a> property of the 
<a href="/windows/desktop/Msi/error-object">Error</a> object. This function returns the <b>LANGID</b> of the error.

## -parameters

### -param ErrorLanguage [out]

A pointer to a location in memory that receives the language value causing this error.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Language is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

The function returns -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed. You can determine the type of error by calling <a href="/windows/desktop/api/mergemod/nf-mergemod-imsmerror-get_type">IMsmError::get_Type</a>.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>