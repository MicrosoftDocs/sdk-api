---
UID: NF:inputscope.ITfInputScope.GetInputScopes
title: ITfInputScope::GetInputScopes (inputscope.h)
description: ITfInputScope::GetInputScopes method
helpviewer_keywords: ["GetInputScopes","GetInputScopes method [Text Services Framework]","GetInputScopes method [Text Services Framework]","ITfInputScope interface","ITfInputScope interface [Text Services Framework]","GetInputScopes method","ITfInputScope.GetInputScopes","ITfInputScope::GetInputScopes","_tsf_itfinputscoe_getinputscopes_ref","inputscope/ITfInputScope::GetInputScopes","tsf.itfinputscope_getinputscope"]
old-location: tsf\itfinputscope_getinputscope.htm
tech.root: TSF
ms.assetid: c5d54d2a-13b4-42f7-9224-4e80f0148a86
ms.date: 12/05/2018
ms.keywords: GetInputScopes, GetInputScopes method [Text Services Framework], GetInputScopes method [Text Services Framework],ITfInputScope interface, ITfInputScope interface [Text Services Framework],GetInputScopes method, ITfInputScope.GetInputScopes, ITfInputScope::GetInputScopes, _tsf_itfinputscoe_getinputscopes_ref, inputscope/ITfInputScope::GetInputScopes, tsf.itfinputscope_getinputscope
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
 - ITfInputScope::GetInputScopes
 - inputscope/ITfInputScope::GetInputScopes
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
 - ITfInputScope.GetInputScopes
---

# ITfInputScope::GetInputScopes


## -description

Gets the input scopes that are associated with this context.

## -parameters

### -param pprgInputScopes [out]

Pointer to an array of pointers to the input scopes. The calling function must call <b>CoTaskMemFree()</b> to free the buffer.

### -param pcCount [out]

Pointer to the number of input scopes returned.

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

