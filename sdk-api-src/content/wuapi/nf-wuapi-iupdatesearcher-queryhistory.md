---
UID: NF:wuapi.IUpdateSearcher.QueryHistory
title: IUpdateSearcher::QueryHistory
author: windows-sdk-content
description: Synchronously queries the computer for the history of the update events.
old-location: wua\iupdatesearcher_queryhistory.htm
tech.root: Wua_Sdk
ms.assetid: 4d3027a2-ba97-4dfc-9a15-c106aaf6c2b9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUpdateSearcher interface [Windows Update Agent],QueryHistory method, IUpdateSearcher.QueryHistory, IUpdateSearcher::QueryHistory, QueryHistory, QueryHistory method [Windows Update Agent], QueryHistory method [Windows Update Agent],IUpdateSearcher interface, wua.iupdatesearcher_queryhistory, wuapi/IUpdateSearcher::QueryHistory
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSearcher.QueryHistory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateSearcher::QueryHistory


## -description


Synchronously queries the computer for the history of the update events.


## -parameters




### -param startIndex [in]

The index of the first event to retrieve.


### -param count [in]

The number of events to retrieve.


### -param retval [out]

A pointer to an <a href="https://msdn.microsoft.com/c3bc764b-c9cc-4567-963e-2e481bdda611">IUpdateHistoryEntryCollection</a> interface that contains matching event records on the computer in descending chronological order.


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
<dt><b>WU_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
An index is invalid.

</td>
</tr>
</table>
 




## -remarks



This method returns <b>WU_E_INVALIDINDEX</b> if  the <i>startIndex</i> parameter is less than 0 (zero) or if the <i>Count</i> parameter is less than or equal to 0 (zero).




## -see-also




<a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>
 

 

