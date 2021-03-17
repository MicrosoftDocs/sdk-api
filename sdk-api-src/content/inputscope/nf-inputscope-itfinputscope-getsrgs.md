---
UID: NF:inputscope.ITfInputScope.GetSRGS
title: ITfInputScope::GetSRGS (inputscope.h)
description: ITfInputScope::GetSRGS method
helpviewer_keywords: ["GetSRGS","GetSRGS method [Text Services Framework]","GetSRGS method [Text Services Framework]","ITfInputScope interface","ITfInputScope interface [Text Services Framework]","GetSRGS method","ITfInputScope.GetSRGS","ITfInputScope::GetSRGS","inputscope/ITfInputScope::GetSRGS","tsf.itfinputscope_getSRGS"]
old-location: tsf\itfinputscope_getSRGS.htm
tech.root: TSF
ms.assetid: 6514d925-b60e-4071-abb2-4c26a122089a
ms.date: 12/05/2018
ms.keywords: GetSRGS, GetSRGS method [Text Services Framework], GetSRGS method [Text Services Framework],ITfInputScope interface, ITfInputScope interface [Text Services Framework],GetSRGS method, ITfInputScope.GetSRGS, ITfInputScope::GetSRGS, inputscope/ITfInputScope::GetSRGS, tsf.itfinputscope_getSRGS
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
 - ITfInputScope::GetSRGS
 - inputscope/ITfInputScope::GetSRGS
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
 - ITfInputScope.GetSRGS
---

# ITfInputScope::GetSRGS


## -description

Gets the Speech Recognition Grammar Specification (SRGS) string to be recognized.

## -parameters

### -param pbstrSRGS [out]

The xml string. The calling function must call <b>SysFreeString()</b> to free the buffer.

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

## -remarks

<a href="https://www.w3.org/tr/speech-grammar">http://www.w3.org/TR/speech-grammar</a>

