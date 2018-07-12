---
UID: NF:wuapi.IUpdateSession3.QueryHistory
title: IUpdateSession3::QueryHistory
author: windows-sdk-content
description: Synchronously queries the computer for the history of update events.
old-location: wua\iupdatesession3_queryhistory.htm
old-project: wua_sdk
ms.assetid: 614a392e-949b-4fba-a4e7-5c393c2b51c3
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: IUpdateSession3 interface [Windows Update Agent],QueryHistory method, IUpdateSession3.QueryHistory, IUpdateSession3::QueryHistory, QueryHistory, QueryHistory method [Windows Update Agent], QueryHistory method [Windows Update Agent],IUpdateSession3 interface, wua.iupdatesession3_queryhistory, wuapi/IUpdateSession3::QueryHistory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSession3.QueryHistory
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
 

 

