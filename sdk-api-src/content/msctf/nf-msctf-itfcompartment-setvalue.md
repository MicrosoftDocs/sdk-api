---
UID: NF:msctf.ITfCompartment.SetValue
title: ITfCompartment::SetValue (msctf.h)
description: ITfCompartment::SetValue method
helpviewer_keywords: ["ITfCompartment interface [Text Services Framework]","SetValue method","ITfCompartment.SetValue","ITfCompartment::SetValue","SetValue","SetValue method [Text Services Framework]","SetValue method [Text Services Framework]","ITfCompartment interface","_tsf_itfcompartment_setvalue_ref","msctf/ITfCompartment::SetValue","tsf.itfcompartment_setvalue"]
old-location: tsf\itfcompartment_setvalue.htm
tech.root: TSF
ms.assetid: 1a1a175f-a24e-4f83-92d3-ac6a24f5f486
ms.date: 12/05/2018
ms.keywords: ITfCompartment interface [Text Services Framework],SetValue method, ITfCompartment.SetValue, ITfCompartment::SetValue, SetValue, SetValue method [Text Services Framework], SetValue method [Text Services Framework],ITfCompartment interface, _tsf_itfcompartment_setvalue_ref, msctf/ITfCompartment::SetValue, tsf.itfcompartment_setvalue
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
 - ITfCompartment::SetValue
 - msctf/ITfCompartment::SetValue
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
 - ITfCompartment.SetValue
---

# ITfCompartment::SetValue


## -description

Sets the data for a compartment.

## -parameters

### -param tid [in]

Contains a <a href="/windows/desktop/TSF/tfclientid">TfClientId</a> value that identifies the client.

### -param pvarValue [in]

Pointer to a VARIANT structure that contains the data to be set. Only VT_I4, VT_UNKNOWN and VT_BSTR data types are allowed.

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
<i>pvarValue</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The compartment was cleared by a call to <a href="/windows/desktop/api/msctf/nf-msctf-itfcompartmentmgr-clearcompartment">ITfCompartmentMgr::ClearCompartment</a>, this method was called during a <a href="/windows/desktop/api/msctf/nf-msctf-itfcompartmenteventsink-onchange">ITfCompartmentEventSink::OnChange</a> notification or only the owner can clear this compartment.

</td>
</tr>
</table>

## -see-also

[ITfCompartment interface](nn-msctf-itfcompartment.md), [ITfCompartment::GetValue](nf-msctf-itfcompartment-getvalue.md), [ITfCompartmentMgr::ClearCompartment](nf-msctf-itfcompartmentmgr-clearcompartment.md), [VariantClear function](../oleauto/nf-oleauto-variantclear.md)