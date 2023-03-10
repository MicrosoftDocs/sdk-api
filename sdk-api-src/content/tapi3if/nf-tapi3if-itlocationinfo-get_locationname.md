---
UID: NF:tapi3if.ITLocationInfo.get_LocationName
title: ITLocationInfo::get_LocationName (tapi3if.h)
description: The get_LocationName method gets the location name.
helpviewer_keywords: ["ITLocationInfo interface [TAPI 2.2]","get_LocationName method","ITLocationInfo.get_LocationName","ITLocationInfo::get_LocationName","_tapi3_itlocationinfo_get_locationname","get_LocationName","get_LocationName method [TAPI 2.2]","get_LocationName method [TAPI 2.2]","ITLocationInfo interface","tapi3.itlocationinfo_get_locationname","tapi3if/ITLocationInfo::get_LocationName"]
old-location: tapi3\itlocationinfo_get_locationname.htm
tech.root: tapi3
ms.assetid: 2bd86295-8240-477d-90aa-f3061666c5e6
ms.date: 12/05/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_LocationName method, ITLocationInfo.get_LocationName, ITLocationInfo::get_LocationName, _tapi3_itlocationinfo_get_locationname, get_LocationName, get_LocationName method [TAPI 2.2], get_LocationName method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_locationname, tapi3if/ITLocationInfo::get_LocationName
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
 - ITLocationInfo::get_LocationName
 - tapi3if/ITLocationInfo::get_LocationName
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
 - ITLocationInfo.get_LocationName
---

# ITLocationInfo::get_LocationName


## -description

The 
<b>get_LocationName</b> method gets the location name.

## -parameters

### -param ppLocationName [out]

Pointer to the <b>BSTR</b> representation of the location name.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppLocationName</i> parameter is not a valid pointer.

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
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppLocationName</i> parameter.
			

The value that this method returns corresponds to the <b>dwLocationNameSize</b> and <b>dwLocationNameOffset</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>