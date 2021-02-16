---
UID: NF:msctf.ITfCompartmentMgr.EnumCompartments
title: ITfCompartmentMgr::EnumCompartments (msctf.h)
description: The ITfCompartmentMgr::EnumCompartments method obtains an enumerator that contains the GUID of the compartments within the compartment manager.
helpviewer_keywords: ["EnumCompartments","EnumCompartments method [Text Services Framework]","EnumCompartments method [Text Services Framework]","ITfCompartmentMgr interface","ITfCompartmentMgr interface [Text Services Framework]","EnumCompartments method","ITfCompartmentMgr.EnumCompartments","ITfCompartmentMgr::EnumCompartments","_tsf_itfcompartmentmgr_enumcompartments_ref","msctf/ITfCompartmentMgr::EnumCompartments","tsf.itfcompartmentmgr_enumcompartments"]
old-location: tsf\itfcompartmentmgr_enumcompartments.htm
tech.root: TSF
ms.assetid: d8c90637-dd6d-425f-9d5d-44c7dbfcf8a5
ms.date: 12/05/2018
ms.keywords: EnumCompartments, EnumCompartments method [Text Services Framework], EnumCompartments method [Text Services Framework],ITfCompartmentMgr interface, ITfCompartmentMgr interface [Text Services Framework],EnumCompartments method, ITfCompartmentMgr.EnumCompartments, ITfCompartmentMgr::EnumCompartments, _tsf_itfcompartmentmgr_enumcompartments_ref, msctf/ITfCompartmentMgr::EnumCompartments, tsf.itfcompartmentmgr_enumcompartments
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
 - ITfCompartmentMgr::EnumCompartments
 - msctf/ITfCompartmentMgr::EnumCompartments
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
 - ITfCompartmentMgr.EnumCompartments
---

# ITfCompartmentMgr::EnumCompartments


## -description

The <b>ITfCompartmentMgr::EnumCompartments</b> method obtains an enumerator that contains the GUID of the compartments within the compartment manager.

## -parameters

### -param ppEnum [out]

Pointer to an <b>IEnumGUID</b> interface pointer that receives the enumerator object.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppcEnum</i> is invalid.

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

