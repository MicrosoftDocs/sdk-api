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

# IUpdateSession3::QueryHistory


## -description


Synchronously queries the computer for the history of update events. This method method returns a pointer to an <a href="https://msdn.microsoft.com/c3bc764b-c9cc-4567-963e-2e481bdda611">IUpdateHistoryEntryCollection</a> interface that contains matching event records on the  computer.


## -parameters




### -param criteria [in]

A string that specifies the search criteria.


### -param startIndex [in]

The index of the first event to retrieve.


### -param count [in]

The number of events to retrieve.


### -param retval [out]

A pointer to an <a href="https://msdn.microsoft.com/c3bc764b-c9cc-4567-963e-2e481bdda611">IUpdateHistoryEntryCollection</a> interface that contains the matching event records on the computer in descending chronological order.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_CRITERIA</b></dt>
</dl>
</td>
<td width="60%">
There is an invalid search criteria.

</td>
</tr>
</table>
 




## -remarks



The collection of events that is returned is sorted by the date in descending order.

The string that is used for  the <i>criteria</i> parameter must match the custom search language for <b>QueryHistory</b>. The string contains criteria that are evaluated to determine which history events to return.

Note that <b>QueryHistory</b> supports per-machine updates only.

For a complete description of search criteria syntax, see <a href="https://msdn.microsoft.com/library/windows/hardware/mt219145">Search</a>. 

The following table identifies all the public support criteria, in the order of evaluation precedence. More criteria may be added to this list in the future.

<table>
<tr>
<th>Criterion</th>
<th>Type</th>
<th>Allowed operators</th>
<th>Description</th>
</tr>
<tr>
<td>UpdateID</td>
<td><b>string(UUID)</b></td>
<td><b>=</b></td>
<td>
Finds updates that have an <a href="https://msdn.microsoft.com/072c85a7-bcac-4323-97df-75aa2b89f1ba">UpdateIdentity.UpdateID</a> of the specified value. 

For example, "UpdateID='12345678-9abc-def0-1234-56789abcdef0'" finds updates for <a href="https://msdn.microsoft.com/072c85a7-bcac-4323-97df-75aa2b89f1ba">UpdateIdentity.UpdateID</a> that equal 12345678-9abc-def0-1234-56789abcdef0.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7caa07ee-ec78-45eb-99a2-0e6682790c88">IUpdateSession3</a>
 

 

