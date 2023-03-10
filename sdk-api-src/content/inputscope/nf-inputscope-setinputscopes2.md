---
UID: NF:inputscope.SetInputScopes2
title: SetInputScopes2 function (inputscope.h)
description: The application must call SetInputScope with IS_DEFAULT before a window is destroyed to clear the reference of the interface.
helpviewer_keywords: ["SetInputScopes2","SetInputScopes2 function [Text Services Framework]","inputscope/SetInputScopes2","tsf.SetInputScopes2"]
old-location: tsf\SetInputScopes2.htm
tech.root: TSF
ms.assetid: 0b3e0e98-412f-4c6f-aa06-a7f17f8869ac
ms.date: 12/05/2018
ms.keywords: SetInputScopes2, SetInputScopes2 function [Text Services Framework], inputscope/SetInputScopes2, tsf.SetInputScopes2
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
 - SetInputScopes2
 - inputscope/SetInputScopes2
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
 - SetInputScopes2
---

# SetInputScopes2 function


## -description

The application must call <a href="/windows/desktop/api/inputscope/nf-inputscope-setinputscope">SetInputScope</a> with IS_DEFAULT before a window is destroyed to clear the reference of the interface.

## -parameters

### -param hwnd [in]

The window to set the scope on. This call will replace whatever scope may have been on the hwnd before.

### -param pInputScopes [in]

Pointer to an array of input scopes. May be <b>NULL</b>. If not <b>NULL</b>, all of the scopes contained within will be set as the input scope of the hwnd with equal weighting. Use IS_DEFAULT to accept all other input as well (this is the "don’t coerce" option).

### -param cInputScopes [in]

A count of the number of input scopes in <i>pInputScopes</i>. Must be zero if rgScopes is <b>NULL</b>, must be nonzero if <i>pInputScopes</i> is non-<b>NULL</b>.

### -param pEnumString [in]

IenumString interface pointer of the phrase list.

### -param pszRegExp [in]

Pointer to a <b>NULL</b>-terminated string describing the regular expression to be recognized. May be <b>NULL</b>.

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
<td>The input scope set or cleared successfully.</td>
</tr>
</table>

## -remarks

The application must call <a href="/windows/desktop/api/inputscope/nf-inputscope-setinputscope">SetInputScope</a> with IS_DEFAULT before a window is destroyed to clear the reference of the interface.

If you call this method on a window (<i>hwnd</i> parameter) that has 
not been associated with a Document Manager, then no text service notifications are sent to interested clients (such as the touch keyboard) that may want to respond to the 
scope change.