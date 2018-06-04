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

# GetProcessWorkingSetSizeEx function


## -description


Retrieves the minimum and maximum working set sizes of the specified process.


## -parameters




### -param hProcess [in]

A handle to the process whose working set sizes will be obtained. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.


### -param lpMinimumWorkingSetSize [out]

A pointer to a variable that receives the minimum working set size of the specified process, in bytes. The virtual memory manager attempts to keep at least this much memory resident in the process whenever the process is active.


### -param lpMaximumWorkingSetSize [out]

A pointer to a variable that receives the maximum working set size of the specified process, in bytes. The virtual memory manager attempts to keep no more than this much memory resident in the process whenever the process is active when memory is in short supply.


### -param Flags [out]

The flags that control the enforcement of the minimum and maximum working set sizes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MIN_DISABLE"></a><a id="quota_limits_hardws_min_disable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MIN_DISABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The working set may fall below the minimum working set limit if memory demands are high.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MIN_ENABLE"></a><a id="quota_limits_hardws_min_enable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MIN_ENABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The working set will not fall below the minimum working set limit.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MAX_DISABLE"></a><a id="quota_limits_hardws_max_disable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MAX_DISABLE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The working set may exceed the maximum working set limit if there is abundant memory.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MAX_ENABLE"></a><a id="quota_limits_hardws_max_enable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MAX_ENABLE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The working set will not exceed the maximum working set limit.

</td>
</tr>
</table>
 


## -remarks



The "working set" of a process is the set of memory pages currently visible to the process in physical RAM memory. These pages are resident and available for an application to use without triggering a page fault. The minimum and maximum working set sizes affect the virtual memory paging behavior of a process.




## -see-also




<a href="https://msdn.microsoft.com/6017ef59-d2e9-4245-a406-8965024dbb35">Process Working Set</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/04332239-dfc2-4d32-987a-af187e725b71">SetProcessWorkingSetSizeEx</a>
 

 

