---
UID: NF:combaseapi.CoGetCallerTID
title: CoGetCallerTID function
author: windows-sdk-content
description: Returns a pointer to a DWORD that contains the apartment ID of the caller's thread.
old-location: com\cogetcallertid.htm
tech.root: com
ms.assetid: 3a34001b-6286-4103-ae9f-700ea101dc17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CoGetCallerTID, CoGetCallerTID function [COM], _com_CoGetCallerTID, com.cogetcallertid, combaseapi/CoGetCallerTID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetCallerTID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoGetCallerTID function


## -description


Returns a pointer to a <b>DWORD</b> that contains the apartment ID of the caller's thread.


## -parameters




### -param lpdwTID [out]

Receives the apartment ID of the caller's thread. For a single threaded apartment (STA), this is the current thread ID. For a multithreaded apartment (MTA), the value is 0.  For a neutral apartment (NA), the value is -1.


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
<dt><b>S_TRUE</b></dt>
</dl>
</td>
<td width="60%">
The caller's thread ID is set and the caller is in the same process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The caller's thread ID is set and the caller is in a different process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller's thread ID was not set.

</td>
</tr>
</table>
 




## -remarks



If the caller is not running on the same computer, this function does not return the apartment ID and the return value is S_FALSE.

There is no guarantee that the information returned from this API is not tampered with, so do not use the ID that is returned to make security decisions. The ID can only be used for logging and diagnostic purposes.



