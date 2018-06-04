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

# MgmGroupEnumerationStart function


## -description


The 
<b>MgmGroupEnumerationStart</b> function obtains an enumeration handle that is later used to obtain the list of groups that have been joined. After the client obtains the handle, it should use the 
<a href="https://msdn.microsoft.com/a5e659e9-b566-490b-831b-96f9de822ebf">MgmGroupEnumerationGetNext</a> function to enumerate the groups.


## -parameters




### -param hProtocol [in]

Handle to the protocol obtained from a previous call to 
<a href="https://msdn.microsoft.com/a9b5f5f3-6e54-4a97-b3e7-e9e026947116">MgmRegisterMProtocol</a>.


### -param metEnumType [in]

Specifies the type of enumeration. The following enumerations are available. 



<table>
<tr>
<th>Enumeration</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ALL_SOURCES"></a><a id="all_sources"></a><dl>
<dt><b>ALL_SOURCES</b></dt>
</dl>
</td>
<td width="60%">
Retrieves wildcard joins (*, g) and source-specific joins (s, g).

</td>
</tr>
<tr>
<td width="40%"><a id="ANY_SOURCE"></a><a id="any_source"></a><dl>
<dt><b>ANY_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves group entries that have at least one source specified.

</td>
</tr>
</table>
 


### -param phEnumHandle [out]

Receives the handle to the enumeration. Use this handle in calls to 
<a href="https://msdn.microsoft.com/a5e659e9-b566-490b-831b-96f9de822ebf">MgmGroupEnumerationGetNext</a> and 
<a href="https://msdn.microsoft.com/87a0bd96-c877-443e-a539-a31ab0971869">MgmGroupEnumerationEnd</a>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid handle to a protocol.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete this operation.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/09b60342-25a8-4d0a-8176-3701f0622aa8">MGM_ENUM_TYPES</a>



<a href="https://msdn.microsoft.com/87a0bd96-c877-443e-a539-a31ab0971869">MgmGroupEnumerationEnd</a>



<a href="https://msdn.microsoft.com/a5e659e9-b566-490b-831b-96f9de822ebf">MgmGroupEnumerationGetNext</a>
 

 

