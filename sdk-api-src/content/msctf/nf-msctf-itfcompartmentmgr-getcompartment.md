---
UID: NF:msctf.ITfCompartmentMgr.GetCompartment
title: ITfCompartmentMgr::GetCompartment (msctf.h)
description: ITfCompartmentMgr::GetCompartment method
helpviewer_keywords: ["GetCompartment","GetCompartment method [Text Services Framework]","GetCompartment method [Text Services Framework]","ITfCompartmentMgr interface","ITfCompartmentMgr interface [Text Services Framework]","GetCompartment method","ITfCompartmentMgr.GetCompartment","ITfCompartmentMgr::GetCompartment","_tsf_itfcompartmentmgr_getcompartment_ref","msctf/ITfCompartmentMgr::GetCompartment","tsf.itfcompartmentmgr_getcompartment"]
old-location: tsf\itfcompartmentmgr_getcompartment.htm
tech.root: TSF
ms.assetid: 4f71815b-d352-4303-a3dd-180a71f9a5fe
ms.date: 12/05/2018
ms.keywords: GetCompartment, GetCompartment method [Text Services Framework], GetCompartment method [Text Services Framework],ITfCompartmentMgr interface, ITfCompartmentMgr interface [Text Services Framework],GetCompartment method, ITfCompartmentMgr.GetCompartment, ITfCompartmentMgr::GetCompartment, _tsf_itfcompartmentmgr_getcompartment_ref, msctf/ITfCompartmentMgr::GetCompartment, tsf.itfcompartmentmgr_getcompartment
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
 - ITfCompartmentMgr::GetCompartment
 - msctf/ITfCompartmentMgr::GetCompartment
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
 - ITfCompartmentMgr.GetCompartment
---

# ITfCompartmentMgr::GetCompartment


## -description

Obtains the compartment object for a specified compartment.

## -parameters

### -param rguid [in]

Contains a GUID that identifies the compartment.

### -param ppcomp [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcompartment">ITfCompartment</a> interface pointer that receives the compartment object.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppcomp</i> is invalid.

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
</table>

## -see-also

[ITfCompartmentMgr interface](nn-msctf-itfcompartmentmgr.md), [ITfCompartment interface](nn-msctf-itfcompartment.md), [Compartments](/windows/desktop/TSF/compartments)