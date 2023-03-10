---
UID: NF:inputscope.SetInputScopes
title: SetInputScopes function (inputscope.h)
description: Sets a combination of one input scope, multiple input scopes, one phrase list, a regular expression, and/or Speech Recognition Grammar Specification (SRGS) rules for the specified window.
helpviewer_keywords: ["SetInputScopes","SetInputScopes function [Text Services Framework]","inputscope/SetInputScopes","tsf.SetInputScopes"]
old-location: tsf\SetInputScopes.htm
tech.root: TSF
ms.assetid: 28c0be9b-f42c-4ab1-a3af-9c591a5192dd
ms.date: 12/05/2018
ms.keywords: SetInputScopes, SetInputScopes function [Text Services Framework], inputscope/SetInputScopes, tsf.SetInputScopes
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetInputScopes
 - inputscope/SetInputScopes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - msctf.dll
api_name:
 - SetInputScopes
---

# SetInputScopes function


## -description

Sets a combination of one input scope, multiple input scopes, one phrase list, a regular expression, and/or Speech Recognition Grammar Specification (SRGS) rules for the specified window.

## -parameters

### -param hwnd [in]

The window to set the scope on.

### -param pInputScopes [in]

Pointer to an array of input scopes. Can be <b>NULL</b>. If not <b>NULL</b>, all of the input scopes in the array are set as the input scope of the window with equal weighting. Use IS_DEFAULT to accept all other input scopes as well.

### -param cInputScopes [in]

The number of input scopes in the array pointed to by <i>*pInputScopes</i>. This value must be zero if the array is <b>NULL</b>.

### -param ppszPhraseList [in]

Pointer to an array of pointers to <b>NULL</b>-terminated phrases. Can be <b>NULL</b>.

### -param cPhrases [in]

Number of pointers pointed to by <i>**ppszPhraseList</i>, which represents the number of phrases.

### -param pszRegExp [in]

Pointer to a <b>NULL</b>-terminated string containing the regular expression to be recognized. Can be <b>NULL</b>.

### -param pszSRGS [in]

Pointer to a <b>NULL</b>-terminated XML string that provides speech-specific hints and rules to aid in speech recognition. The XML format conforms to the Speech Recognition Grammar Specification (SRGS) standard, outlined at <a href="https://www.w3.org/tr/speech-grammar">http://www.w3.org/TR/speech-grammar</a>. Can be <b>NULL</b>. $

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method was successful.</td>
</tr>
</table>

## -remarks

Calling this method replaces whatever scope is associated with the window.

This API works only when the window (hwnd parameter) and the calling thread are in the same thread. If you call this API for a different thread's window, it fails with E_INVALIDARG.

If you call this method on a window (<i>hwnd</i> parameter) that has 
not been associated with a Document Manager, then no text service notifications are sent to interested clients (such as the touch keyboard) that may want to respond to the 
scope change.

