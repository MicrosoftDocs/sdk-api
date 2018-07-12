---
UID: NF:perflib.PerfEnumerateCounterSetInstances
title: PerfEnumerateCounterSetInstances function
author: windows-sdk-content
description: Gets the names and identifiers of the active instances of a counter set on the specified system.
old-location: perf\perfenumeratecountersetinstances.htm
old-project: perfctrs
ms.assetid: 83DCEAB7-5F79-4A55-8BAC-D20F545FF76D
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: PerfEnumerateCounterSetInstances, PerfEnumerateCounterSetInstances function [Perf], perf.perfenumeratecountersetinstances, perflib/PerfEnumerateCounterSetInstances
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: PerfRegInfoType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - AdvAPI32.dll
api_name:
 - PerfEnumerateCounterSetInstances
product: Windows
targetos: Windows
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
req.product: ADAM
---

# PerfEnumerateCounterSetInstances function


## -description


Gets the names and identifiers of the active instances of a counter set on the  

specified system.  



## -parameters




### -param szMachine [in, optional]

The name of the machine for which to get the information about the active instances of the counter set  that the <i>pCounterSet</i> parameter specifies. If NULL, the function retrieves information about the active instances of the specified counter set for the local machine.


### -param pCounterSetId [in]

The counter set identifier of the counter set for which you want to get the information about of the active instances.


### -param pInstances [out, optional]

Pointer to a buffer that is large enough to receive the amount of data that the <i>cbInstances</i> parameter specifies. May be  

NULL if <i>cbInstances</i> is 0.  



### -param cbInstances

The size of the buffer that the  <i>pInstances</i> parameter specifies,  in bytes.  



### -param pcbInstancesActual [out]

The size of the buffer actually required to get the information about of the active instances. The meaning depends on the value that the function  

returns.

<table>
<tr>
<th>Function  Return Value</th>
<th>Meaning of <i>pcbInstancesActual</i></th>
</tr>
<tr>
<td><b>ERROR_SUCCESS</b></td>
<td>The number of  

  bytes of information about the active instances of the specified counter set that the function stored in the buffer that <i>pInstances</i> specified.</td>
</tr>
<tr>
<td><b> ERROR_NOT_ENOUGH_MEMORY</b></td>
<td>The  

  size of the buffer required to store the information about the active instances of the counter set on the specified machine, in bytes. Enlarge the buffer to the required  

  size and call the function again.  

</td>
</tr>
<tr>
<td>Other</td>
<td>The value is undefined and should not be used.</td>
</tr>
</table>
 


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function successfully stored all of the information about the active instances of the counter set in the buffer that <i>pInstances</i> specified. The value that <i>pcbInstancesActual</i> points to indicates amount of information actually stored in the buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
 The buffer that <i>pInstances</i> specified was not large enough to store all of the information about the active instances of the counter set.  The value that <i>pcbInstancesActual</i> points to  indicates the size of the buffer required to store all of the information. Enlarge the buffer to the required  

  size and call the function again.  



</td>
</tr>
</table>
 


						
						For other types of failures, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 
					




## -remarks



The information about the active instances of the specified counter set is  written to the buffer that <i>pInstances</i> specifies as a sequence of <a href="https://msdn.microsoft.com/58E4062A-0CE4-4FF7-A9B2-CA0947563C7B">PERF_INSTANCE_HEADER</a> blocks. The size in bytes of  

the sequence of blocks is written to  <i>pcbInstancesActual</i>. Each <b>PERF_INSTANCE_HEADER</b> block consists  

of a <b>PERF_INSTANCE_HEADER</b> structure, immediately followed by a null-terminated UTF-16LE  

instance name, followed by padding so that the size of the  

<b>PERF_INSTANCE_HEADER</b> block is a multiple of 8 bytes. 





## -see-also




<a href="https://msdn.microsoft.com/58E4062A-0CE4-4FF7-A9B2-CA0947563C7B">PERF_INSTANCE_HEADER</a>



<a href="https://msdn.microsoft.com/6C487D11-2DC0-475C-AA0F-4060641C6500">PerfEnumerateCounterSet</a>
 

 

