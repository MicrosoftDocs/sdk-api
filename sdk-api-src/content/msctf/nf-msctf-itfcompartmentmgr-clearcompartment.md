---
UID: NF:msctf.ITfCompartmentMgr.ClearCompartment
title: ITfCompartmentMgr::ClearCompartment (msctf.h)
description: ITfCompartmentMgr::ClearCompartment method
helpviewer_keywords: ["ClearCompartment","ClearCompartment method [Text Services Framework]","ClearCompartment method [Text Services Framework]","ITfCompartmentMgr interface","ITfCompartmentMgr interface [Text Services Framework]","ClearCompartment method","ITfCompartmentMgr.ClearCompartment","ITfCompartmentMgr::ClearCompartment","_tsf_itfcompartmentmgr_clearcompartment_ref","msctf/ITfCompartmentMgr::ClearCompartment","tsf.itfcompartmentmgr_clearcompartment"]
old-location: tsf\itfcompartmentmgr_clearcompartment.htm
tech.root: TSF
ms.assetid: 862ec077-b192-412a-b80c-6105f503ed21
ms.date: 12/05/2018
ms.keywords: ClearCompartment, ClearCompartment method [Text Services Framework], ClearCompartment method [Text Services Framework],ITfCompartmentMgr interface, ITfCompartmentMgr interface [Text Services Framework],ClearCompartment method, ITfCompartmentMgr.ClearCompartment, ITfCompartmentMgr::ClearCompartment, _tsf_itfcompartmentmgr_clearcompartment_ref, msctf/ITfCompartmentMgr::ClearCompartment, tsf.itfcompartmentmgr_clearcompartment
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
 - ITfCompartmentMgr::ClearCompartment
 - msctf/ITfCompartmentMgr::ClearCompartment
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
 - ITfCompartmentMgr.ClearCompartment
---

# ITfCompartmentMgr::ClearCompartment


## -description

Removes the specified compartment.

## -parameters

### -param tid [in]

Contains a <a href="/windows/desktop/TSF/tfclientid">TfClientId</a> value that identifies the client.

### -param rguid [in]

Contains a GUID that identifies the compartment.

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
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The compartment cannot be found.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The owner must clear this compartment.

</td>
</tr>
</table>

## -see-also

[ITfCompartmentMgr interface](nn-msctf-itfcompartmentmgr.md), [ITfCompartment interface](nn-msctf-itfcompartment.md), [Compartments](/windows/desktop/TSF/compartments)