---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# LogTimeProvEventFunc callback function


## -description


Logs a time provider event in the event log.


## -parameters




### -param wType [in]

The event type. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Error"></a><a id="error"></a><a id="ERROR"></a><dl>
<dt><b>Error</b></dt>
</dl>
</td>
<td width="60%">
Indicates a significant problem.

</td>
</tr>
<tr>
<td width="40%"><a id="Information"></a><a id="information"></a><a id="INFORMATION"></a><dl>
<dt><b>Information</b></dt>
</dl>
</td>
<td width="60%">
Provides information about a successful operation.

</td>
</tr>
<tr>
<td width="40%"><a id="Warning"></a><a id="warning"></a><a id="WARNING"></a><dl>
<dt><b>Warning</b></dt>
</dl>
</td>
<td width="60%">
Indicates a problem that is not immediately significant, but may cause future problems.

</td>
</tr>
</table>
 


### -param *wszProvName [in]

The provider name.


### -param *wszMessage [in]

The event description.


## -returns



If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.




## -remarks



This function provides the time provider with a simplified interface for event logging. Time providers that require more extensive event logging can perform their own event logging. For more information on event logging, see 
<a href="https://msdn.microsoft.com/5ec95938-ac5d-4f63-9080-2de71454eb17">Event Logging</a>.

The 
<a href="https://msdn.microsoft.com/cf4f8d00-4c6f-4036-a179-444ff7505ab4">TimeProvOpen</a> function returns a pointer to this function.




## -see-also




<a href="https://msdn.microsoft.com/cf4f8d00-4c6f-4036-a179-444ff7505ab4">TimeProvOpen</a>
 

 

