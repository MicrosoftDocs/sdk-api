---
UID: NF:combaseapi.CLSIDFromProgID
title: CLSIDFromProgID function (combaseapi.h)
description: Looks up a CLSID in the registry, given a ProgID.
helpviewer_keywords: ["CLSIDFromProgID","CLSIDFromProgID function [COM]","_com_CLSIDFromProgID","com.clsidfromprogid","combaseapi/CLSIDFromProgID"]
old-location: com\clsidfromprogid.htm
tech.root: com
ms.assetid: 89fb20af-65bf-4ed4-9f71-eb707ee8eb09
ms.date: 12/05/2018
ms.keywords: CLSIDFromProgID, CLSIDFromProgID function [COM], _com_CLSIDFromProgID, com.clsidfromprogid, combaseapi/CLSIDFromProgID
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLSIDFromProgID
 - combaseapi/CLSIDFromProgID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CLSIDFromProgID
---

# CLSIDFromProgID function


## -description

Looks up a CLSID in the registry, given a ProgID.

## -parameters

### -param lpszProgID [in]

A pointer to the ProgID whose CLSID is requested.

### -param lpclsid [out]

Receives a pointer to the retrieved CLSID on return.

## -returns

This function can return the following values.

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
The CLSID was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSSTRING</b></dt>
</dl>
</td>
<td width="60%">
The registered CLSID for the ProgID is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_WRITEREGDB</b></dt>
</dl>
</td>
<td width="60%">
An error occurred writing the CLSID to the registry. See Remarks below.


</td>
</tr>
</table>

## -remarks

Given a ProgID, <b>CLSIDFromProgID</b> looks up its associated CLSID in the registry. If the ProgID cannot be found in the registry, <b>CLSIDFromProgID</b> creates an OLE 1 CLSID for the ProgID and a CLSID entry in the registry. Because of the restrictions placed on OLE 1 CLSID values, <b>CLSIDFromProgID</b> and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromstring">CLSIDFromString</a> are the only two functions that can be used to generate a CLSID for an OLE 1 object.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogidex">CLSIDFromProgIDEx</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid">ProgIDFromCLSID</a>