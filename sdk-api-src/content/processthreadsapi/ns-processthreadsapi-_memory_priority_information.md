---
UID: NS:processthreadsapi._MEMORY_PRIORITY_INFORMATION
title: "_MEMORY_PRIORITY_INFORMATION"
author: windows-sdk-content
description: Specifies the memory priority for a thread or process.
old-location: base\memory_priority_information.htm
old-project: procthread
ms.assetid: 03cacfdf-5c66-42e4-bfcf-afaacd3ad038
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PMEMORY_PRIORITY_INFORMATION, MEMORY_PRIORITY_BELOW_NORMAL, MEMORY_PRIORITY_INFORMATION, MEMORY_PRIORITY_INFORMATION structure, MEMORY_PRIORITY_LOW, MEMORY_PRIORITY_MEDIUM, MEMORY_PRIORITY_NORMAL, MEMORY_PRIORITY_VERY_LOW, PMEMORY_PRIORITY_INFORMATION, PMEMORY_PRIORITY_INFORMATION structure pointer, _MEMORY_PRIORITY_INFORMATION, base.memory_priority_information, processthreadsapi/MEMORY_PRIORITY_INFORMATION, processthreadsapi/PMEMORY_PRIORITY_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: processthreadsapi.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MEMORY_PRIORITY_INFORMATION, *PMEMORY_PRIORITY_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - MEMORY_PRIORITY_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _MEMORY_PRIORITY_INFORMATION structure


## -description


Specifies the memory priority for a thread or process. This structure is used by the <a href="https://msdn.microsoft.com/2b075405-b7b6-4da0-b78d-45eaa9c6c8cd">GetProcessInformation</a>, <a href="https://msdn.microsoft.com/1739fadf-6b43-4b89-8a17-87d9867d5197">SetProcessInformation</a>, <a href="https://msdn.microsoft.com/b7996647-78ab-4f32-bcf6-41aa87d13bb8">GetThreadInformation</a>, and <a href="https://msdn.microsoft.com/c0159bea-870a-46b7-a350-91fe52efae49">SetThreadInformation</a> functions.


## -struct-fields




### -field MemoryPriority

The memory priority for the thread or process.  This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_VERY_LOW"></a><a id="memory_priority_very_low"></a><dl>
<dt><b>MEMORY_PRIORITY_VERY_LOW</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Very low memory priority.

</td>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_LOW"></a><a id="memory_priority_low"></a><dl>
<dt><b>MEMORY_PRIORITY_LOW</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Low memory priority.

</td>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_MEDIUM"></a><a id="memory_priority_medium"></a><dl>
<dt><b>MEMORY_PRIORITY_MEDIUM</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Medium memory priority.

</td>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_BELOW_NORMAL"></a><a id="memory_priority_below_normal"></a><dl>
<dt><b>MEMORY_PRIORITY_BELOW_NORMAL</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Below normal memory priority.

</td>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_NORMAL"></a><a id="memory_priority_normal"></a><dl>
<dt><b>MEMORY_PRIORITY_NORMAL</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Normal memory priority. This is the default priority for all threads and processes on the system.

</td>
</tr>
</table>
 


## -remarks



The memory priority of a thread or process serves as a hint to the memory manager when it trims pages from the working set. Other factors being equal, pages with lower memory priority are trimmed before pages with higher memory priority. For more information, see <a href="https://msdn.microsoft.com/ff05276a-1d40-4844-b649-10e32e3f1937">Working Set</a>.




## -see-also




<a href="https://msdn.microsoft.com/2b075405-b7b6-4da0-b78d-45eaa9c6c8cd">GetProcessInformation</a>



<a href="https://msdn.microsoft.com/b7996647-78ab-4f32-bcf6-41aa87d13bb8">GetThreadInformation</a>



<a href="https://msdn.microsoft.com/1739fadf-6b43-4b89-8a17-87d9867d5197">SetProcessInformation</a>



<a href="https://msdn.microsoft.com/c0159bea-870a-46b7-a350-91fe52efae49">SetThreadInformation</a>
 

 

