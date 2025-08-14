---
UID: NF:combaseapi.CoCreateGuid
title: CoCreateGuid function (combaseapi.h)
description: Creates a GUID, a unique 128-bit integer used for CLSIDs and interface identifiers.
helpviewer_keywords: ["CoCreateGuid","CoCreateGuid function [COM]","_com_CoCreateGuid","com.cocreateguid","combaseapi/CoCreateGuid"]
old-location: com\cocreateguid.htm
tech.root: com
ms.assetid: 8d5cedea-8c2b-4918-99db-1a000989f178
ms.date: 12/05/2018
ms.keywords: CoCreateGuid, CoCreateGuid function [COM], _com_CoCreateGuid, com.cocreateguid, combaseapi/CoCreateGuid
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - CoCreateGuid
 - combaseapi/CoCreateGuid
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
 - CoCreateGuid
---

# CoCreateGuid function


## -description

Creates a GUID, a unique 128-bit integer used for CLSIDs and interface identifiers.

## -parameters

### -param pguid [out]

A pointer to the requested GUID.

## -returns

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
The GUID was successfully created.

</td>
</tr>
</table>
 

Errors returned by <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a> are wrapped as an <b>HRESULT</b>.

## -remarks

The <b>CoCreateGuid</b> function calls the RPC function <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>, which creates a GUID, a globally unique 128-bit integer. Use <b>CoCreateGuid</b> when you need an absolutely unique number that you will use as a persistent identifier in a distributed environment. To a very high degree of certainty, this function returns a unique value – no other invocation, on the same or any other system (networked or not), should return the same value.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>
