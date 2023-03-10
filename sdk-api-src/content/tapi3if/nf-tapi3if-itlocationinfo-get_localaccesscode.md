---
UID: NF:tapi3if.ITLocationInfo.get_LocalAccessCode
title: ITLocationInfo::get_LocalAccessCode (tapi3if.h)
description: The get_LocalAccessCode method gets the local access code.
helpviewer_keywords: ["ITLocationInfo interface [TAPI 2.2]","get_LocalAccessCode method","ITLocationInfo.get_LocalAccessCode","ITLocationInfo::get_LocalAccessCode","_tapi3_itlocationinfo_get_localaccesscode","get_LocalAccessCode","get_LocalAccessCode method [TAPI 2.2]","get_LocalAccessCode method [TAPI 2.2]","ITLocationInfo interface","tapi3.itlocationinfo_get_localaccesscode","tapi3if/ITLocationInfo::get_LocalAccessCode"]
old-location: tapi3\itlocationinfo_get_localaccesscode.htm
tech.root: tapi3
ms.assetid: 15e13c34-911f-4e4f-b7d9-f044bfb6c6d0
ms.date: 12/05/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_LocalAccessCode method, ITLocationInfo.get_LocalAccessCode, ITLocationInfo::get_LocalAccessCode, _tapi3_itlocationinfo_get_localaccesscode, get_LocalAccessCode, get_LocalAccessCode method [TAPI 2.2], get_LocalAccessCode method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_localaccesscode, tapi3if/ITLocationInfo::get_LocalAccessCode
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITLocationInfo::get_LocalAccessCode
 - tapi3if/ITLocationInfo::get_LocalAccessCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLocationInfo.get_LocalAccessCode
---

# ITLocationInfo::get_LocalAccessCode


## -description

The 
<b>get_LocalAccessCode</b> method gets the local access code.

## -parameters

### -param ppCode [out]

Pointer to <b>BSTR</b> representation of local access code.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCode</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCode</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppCode</i> parameter.
			

The value that this method returns corresponds to the <b>dwLocalAccessCodeSize</b> and <b>dwLocalAccessCodeOffset</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>