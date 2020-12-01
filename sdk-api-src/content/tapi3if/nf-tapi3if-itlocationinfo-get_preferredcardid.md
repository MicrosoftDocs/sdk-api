---
UID: NF:tapi3if.ITLocationInfo.get_PreferredCardID
title: ITLocationInfo::get_PreferredCardID (tapi3if.h)
description: The get_PreferredCardID method gets the preferred calling card identifier for dialing from the current location.
helpviewer_keywords: ["ITLocationInfo interface [TAPI 2.2]","get_PreferredCardID method","ITLocationInfo.get_PreferredCardID","ITLocationInfo::get_PreferredCardID","_tapi3_itlocationinfo_get_preferredcardid","get_PreferredCardID","get_PreferredCardID method [TAPI 2.2]","get_PreferredCardID method [TAPI 2.2]","ITLocationInfo interface","tapi3.itlocationinfo_get_preferredcardid","tapi3if/ITLocationInfo::get_PreferredCardID"]
old-location: tapi3\itlocationinfo_get_preferredcardid.htm
tech.root: tapi3
ms.assetid: 7881a005-1bab-47a1-a657-31584d3f2713
ms.date: 12/05/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_PreferredCardID method, ITLocationInfo.get_PreferredCardID, ITLocationInfo::get_PreferredCardID, _tapi3_itlocationinfo_get_preferredcardid, get_PreferredCardID, get_PreferredCardID method [TAPI 2.2], get_PreferredCardID method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_preferredcardid, tapi3if/ITLocationInfo::get_PreferredCardID
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
 - ITLocationInfo::get_PreferredCardID
 - tapi3if/ITLocationInfo::get_PreferredCardID
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
 - ITLocationInfo.get_PreferredCardID
---

# ITLocationInfo::get_PreferredCardID


## -description

The 
<b>get_PreferredCardID</b> method gets the preferred calling card identifier for dialing from the current location.

## -parameters

### -param plCardID [out]

Calling card ID.

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
The <i>plCardID</i> parameter is not a valid pointer.

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

The value that this method returns corresponds to the <b>dwPreferredCardID</b> member of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>