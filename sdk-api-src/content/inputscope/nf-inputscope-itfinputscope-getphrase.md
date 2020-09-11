---
UID: NF:inputscope.ITfInputScope.GetPhrase
title: ITfInputScope::GetPhrase (inputscope.h)
description: ITfInputScope::GetPhrase method
helpviewer_keywords: ["GetPhrase","GetPhrase method [Text Services Framework]","GetPhrase method [Text Services Framework]","ITfInputScope interface","ITfInputScope interface [Text Services Framework]","GetPhrase method","ITfInputScope.GetPhrase","ITfInputScope::GetPhrase","inputscope/ITfInputScope::GetPhrase","tsf.itfinputscope_getphrase"]
old-location: tsf\itfinputscope_getphrase.htm
tech.root: TSF
ms.assetid: 9a97dab0-2e3d-4921-80a6-0f2c79fbf4aa
ms.date: 12/05/2018
ms.keywords: GetPhrase, GetPhrase method [Text Services Framework], GetPhrase method [Text Services Framework],ITfInputScope interface, ITfInputScope interface [Text Services Framework],GetPhrase method, ITfInputScope.GetPhrase, ITfInputScope::GetPhrase, inputscope/ITfInputScope::GetPhrase, tsf.itfinputscope_getphrase
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputScope.idl
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
 - ITfInputScope::GetPhrase
 - inputscope/ITfInputScope::GetPhrase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfInputScope.GetPhrase
---

# ITfInputScope::GetPhrase


## -description

Gets the phrase list set to this context.

## -parameters

### -param ppbstrPhrases [out]

Pointer to an array of pointers to strings containing phrases. The calling function must call <b>SystFreeString()</b> to free the memory allocated to the strings and <b>CoTaskMemFree</b> to free the buffer.

### -param pcCount [out]

Pointer to the number of phrases returned.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

