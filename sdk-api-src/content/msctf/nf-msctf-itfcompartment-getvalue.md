---
UID: NF:msctf.ITfCompartment.GetValue
title: ITfCompartment::GetValue (msctf.h)
description: ITfCompartment::GetValue method
helpviewer_keywords: ["GetValue","GetValue method [Text Services Framework]","GetValue method [Text Services Framework]","ITfCompartment interface","ITfCompartment interface [Text Services Framework]","GetValue method","ITfCompartment.GetValue","ITfCompartment::GetValue","_tsf_itfcompartment_getvalue_ref","msctf/ITfCompartment::GetValue","tsf.itfcompartment_getvalue"]
old-location: tsf\itfcompartment_getvalue.htm
tech.root: TSF
ms.assetid: 31a9efbd-ebde-4877-a387-ebaccd97d732
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Text Services Framework], GetValue method [Text Services Framework],ITfCompartment interface, ITfCompartment interface [Text Services Framework],GetValue method, ITfCompartment.GetValue, ITfCompartment::GetValue, _tsf_itfcompartment_getvalue_ref, msctf/ITfCompartment::GetValue, tsf.itfcompartment_getvalue
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
 - ITfCompartment::GetValue
 - msctf/ITfCompartment::GetValue
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
 - ITfCompartment.GetValue
---

# ITfCompartment::GetValue


## -description

Obtains the data for a compartment.

## -parameters

### -param pvarValue [out]

Pointer to a <b>VARIANT</b> structure that receives the data. This receives VT_EMPTY if the compartment has no value. The caller must free this data when it is no longer required by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>.

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
The compartment has no value. <i>pvarValue</i> receives VT_EMPTY.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The compartment has been cleared by a call to <a href="/windows/desktop/api/msctf/nf-msctf-itfcompartmentmgr-clearcompartment">ITfCompartmentMgr::ClearCompartment</a>.

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
</table>

## -remarks

The caller must recognize the supplied data format in order to use the data. The compartment installer must publish the data format to enable other clients to use it.

## -see-also

[ITfCompartment interface](nn-msctf-itfcompartment.md), [ITfCompartment::SetValue](nf-msctf-itfcompartment-setvalue.md), [ITfCompartmentMgr::ClearCompartment](nf-msctf-itfcompartmentmgr-clearcompartment.md), [VariantClear function](../oleauto/nf-oleauto-variantclear.md)