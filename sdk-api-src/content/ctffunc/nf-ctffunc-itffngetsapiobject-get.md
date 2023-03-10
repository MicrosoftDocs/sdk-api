---
UID: NF:ctffunc.ITfFnGetSAPIObject.Get
title: ITfFnGetSAPIObject::Get (ctffunc.h)
description: ITfFnGetSAPIObject::Get method
helpviewer_keywords: ["Get","Get method [Text Services Framework]","Get method [Text Services Framework]","ITfFnGetSAPIObject interface","ITfFnGetSAPIObject interface [Text Services Framework]","Get method","ITfFnGetSAPIObject.Get","ITfFnGetSAPIObject::Get","_tsf_itffngetsapiobject_get_ref","ctffunc/ITfFnGetSAPIObject::Get","tsf.itffngetsapiobject_get"]
old-location: tsf\itffngetsapiobject_get.htm
tech.root: TSF
ms.assetid: 4dfa2bd2-e25c-4481-ab07-2f764434504d
ms.date: 12/05/2018
ms.keywords: Get, Get method [Text Services Framework], Get method [Text Services Framework],ITfFnGetSAPIObject interface, ITfFnGetSAPIObject interface [Text Services Framework],Get method, ITfFnGetSAPIObject.Get, ITfFnGetSAPIObject::Get, _tsf_itffngetsapiobject_get_ref, ctffunc/ITfFnGetSAPIObject::Get, tsf.itffngetsapiobject_get
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - ITfFnGetSAPIObject::Get
 - ctffunc/ITfFnGetSAPIObject::Get
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
 - ITfFnGetSAPIObject.Get
---

# ITfFnGetSAPIObject::Get


## -description

Obtains a specified SAPI object.

## -parameters

### -param sObj [in]

Contains a <a href="/windows/win32/api/ctffunc/ne-ctffunc-tfsapiobject">TfSapiObject</a> value that specifies the SAPI object to obtain.

### -param ppunk [out]

Pointer to an <b>IUnknown</b> interface pointer that receives the requested SAPI object. The caller must release this interface when it is no longer required.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The requested object cannot be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The requested object is not implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffngetsapiobject">ITfFnGetSAPIObject</a>



<a href="/windows/win32/api/ctffunc/ne-ctffunc-tfsapiobject">TfSapiObject
      </a>