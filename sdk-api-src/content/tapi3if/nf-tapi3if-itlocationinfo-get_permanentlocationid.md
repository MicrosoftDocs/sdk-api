---
UID: NF:tapi3if.ITLocationInfo.get_PermanentLocationID
title: ITLocationInfo::get_PermanentLocationID (tapi3if.h)
description: The get_PermanentLocationID method gets the permanent location identifier.
helpviewer_keywords: ["ITLocationInfo interface [TAPI 2.2]","get_PermanentLocationID method","ITLocationInfo.get_PermanentLocationID","ITLocationInfo::get_PermanentLocationID","_tapi3_itlocationinfo_get_permanentlocationid","get_PermanentLocationID","get_PermanentLocationID method [TAPI 2.2]","get_PermanentLocationID method [TAPI 2.2]","ITLocationInfo interface","tapi3.itlocationinfo_get_permanentlocationid","tapi3if/ITLocationInfo::get_PermanentLocationID"]
old-location: tapi3\itlocationinfo_get_permanentlocationid.htm
tech.root: tapi3
ms.assetid: 5dab6a20-6113-46ef-a5d2-855ac1befc1a
ms.date: 12/05/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_PermanentLocationID method, ITLocationInfo.get_PermanentLocationID, ITLocationInfo::get_PermanentLocationID, _tapi3_itlocationinfo_get_permanentlocationid, get_PermanentLocationID, get_PermanentLocationID method [TAPI 2.2], get_PermanentLocationID method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_permanentlocationid, tapi3if/ITLocationInfo::get_PermanentLocationID
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
 - ITLocationInfo::get_PermanentLocationID
 - tapi3if/ITLocationInfo::get_PermanentLocationID
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
 - ITLocationInfo.get_PermanentLocationID
---

# ITLocationInfo::get_PermanentLocationID


## -description

The 
<b>get_PermanentLocationID</b> method gets the permanent location identifier.

## -parameters

### -param plLocationID [out]

Pointer to the permanent location identifier.

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
The <i>plLocationID</i> parameter is not a valid pointer.

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

The value that this method returns corresponds to the <b>dwPermanentLocationID</b> member of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>