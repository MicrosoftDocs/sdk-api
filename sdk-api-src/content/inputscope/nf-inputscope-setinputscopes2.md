---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SetInputScopes2 function


## -description


The application must call <a href="https://msdn.microsoft.com/4098525c-8d29-419a-9484-9e70420416bc">SetInputScope</a> with IS_DEFAULT before a window is destroyed to clear the reference of the interface.


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

Pointer to a <b>NULL</b>-terminated XML string that provides speech-specific hints and rules to aid in speech recognition. The XML format conforms to the Speech Recognition Grammar Specification (SRGS) standard, outlined at <a href="http://go.microsoft.com/fwlink/p/?linkid=161740">http://www.w3.org/TR/speech-grammar</a>. Can be <b>NULL</b>. $


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



The application must call <a href="https://msdn.microsoft.com/4098525c-8d29-419a-9484-9e70420416bc">SetInputScope</a> with IS_DEFAULT before a window is destroyed to clear the reference of the interface.

If you call this method on a window (<i>hwnd</i> parameter) that has 
not been associated with a Document Manager, then no text service notifications are sent to interested clients (such as the touch keyboard) that may want to respond to the 
scope change.



