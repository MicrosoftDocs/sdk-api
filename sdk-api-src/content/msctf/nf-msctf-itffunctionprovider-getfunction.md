---
UID: NF:msctf.ITfFunctionProvider.GetFunction
title: ITfFunctionProvider::GetFunction (msctf.h)
description: ITfFunctionProvider::GetFunction method
helpviewer_keywords: ["GetFunction","GetFunction method [Text Services Framework]","GetFunction method [Text Services Framework]","ITfFunctionProvider interface","ITfFunctionProvider interface [Text Services Framework]","GetFunction method","ITfFunctionProvider.GetFunction","ITfFunctionProvider::GetFunction","_tsf_itffunctionprovider_getfunction_ref","msctf/ITfFunctionProvider::GetFunction","tsf.itffunctionprovider_getfunction"]
old-location: tsf\itffunctionprovider_getfunction.htm
tech.root: TSF
ms.assetid: a8ec629a-9ac6-4f25-82f2-42af6ce52ddc
ms.date: 12/05/2018
ms.keywords: GetFunction, GetFunction method [Text Services Framework], GetFunction method [Text Services Framework],ITfFunctionProvider interface, ITfFunctionProvider interface [Text Services Framework],GetFunction method, ITfFunctionProvider.GetFunction, ITfFunctionProvider::GetFunction, _tsf_itffunctionprovider_getfunction_ref, msctf/ITfFunctionProvider::GetFunction, tsf.itffunctionprovider_getfunction
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFunctionProvider::GetFunction
 - msctf/ITfFunctionProvider::GetFunction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfFunctionProvider.GetFunction
---

# ITfFunctionProvider::GetFunction


## -description

Obtains the specified function object.

## -parameters

### -param rguid [in]

Contains a GUID value that identifies the function group that the requested function belongs to. This value can be GUID_NULL.

### -param riid [in]

Contains an interface identifier that identifies the requested function within the group specified by <i>rguid</i>. This value can be specified by the application, text service, or one of the IID_ITfFn* values.

### -param ppunk [out]

Pointer to an <b>IUnknown</b> interface pointer that receives the requested function interface.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested function is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

