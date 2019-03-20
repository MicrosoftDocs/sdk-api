---
UID: NF:combaseapi.CoCreateGuid
title: CoCreateGuid function (combaseapi.h)
author: windows-sdk-content
description: Creates a GUID, a unique 128-bit integer used for CLSIDs and interface identifiers.
old-location: com\cocreateguid.htm
tech.root: com
ms.assetid: 8d5cedea-8c2b-4918-99db-1a000989f178
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CoCreateGuid, CoCreateGuid function [COM], _com_CoCreateGuid, com.cocreateguid, combaseapi/CoCreateGuid
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoCreateGuid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

Errors returned by <a href="https://msdn.microsoft.com/4008fb54-7770-4f1a-8e1c-4b20bef884f9">UuidCreate</a> are wrapped as an <b>HRESULT</b>.




## -remarks



The <b>CoCreateGuid</b> function calls the RPC function <a href="https://msdn.microsoft.com/4008fb54-7770-4f1a-8e1c-4b20bef884f9">UuidCreate</a>, which creates a GUID, a globally unique 128-bit integer. Use <b>CoCreateGuid</b> when you need an absolutely unique number that you will use as a persistent identifier in a distributed environment.To a very high degree of certainty, this function returns a unique value – no other invocation, on the same or any other system (networked or not), should return the same value.




## -see-also




<a href="https://msdn.microsoft.com/4008fb54-7770-4f1a-8e1c-4b20bef884f9">UuidCreate</a>
 

 

