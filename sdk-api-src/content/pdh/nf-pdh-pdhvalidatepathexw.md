---
UID: NF:pdh.PdhValidatePathExW
title: PdhValidatePathExW function
author: windows-sdk-content
description: Validates that the specified counter is present on the computer or in the log file.
old-location: perf\pdhvalidatepathex.htm
old-project: PerfCtrs
ms.assetid: e6b52af7-7276-4565-aa61-73899796a13c
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PdhValidatePathEx, PdhValidatePathEx function [Perf], PdhValidatePathExA, PdhValidatePathExW, pdh/PdhValidatePathEx, pdh/PdhValidatePathExA, pdh/PdhValidatePathExW, perf.pdhvalidatepathex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: pdh.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhValidatePathExW (Unicode) and PdhValidatePathExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhValidatePathEx
 - PdhValidatePathExA
 - PdhValidatePathExW
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: ADAM
---

# PdhValidatePathExW function


## -description


Validates that the specified counter is present on the computer or in the log file.
		


## -parameters




### -param hDataSource [in, optional]

Handle to the data source. The <a href="https://msdn.microsoft.com/a8457959-af3a-497f-91ca-0876cbb552cc">PdhOpenLog</a> and <a href="https://msdn.microsoft.com/eaed9b28-eb09-4123-9317-5d3d50e2d77a">PdhBindInputDataSource</a> functions return this handle. 

To validate that the counter is present on the local computer, specify <b>NULL</b> (this is the same as calling <a href="https://msdn.microsoft.com/9248e63c-2672-466f-85f5-46f26e31dc75">PdhValidatePath</a>).


### -param szFullPathBuffer [in]

<b>Null</b>-terminated string that specifies the counter path to validate. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_INSTANCE</b></dt>
</dl>
</td>
<td width="60%">
The specified instance of the performance object was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_COUNTER</b></dt>
</dl>
</td>
<td width="60%">
The specified counter was not found in the performance object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The specified performance object was not found on the computer or in the log file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The specified computer could not be found or connected to.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_BAD_COUNTERNAME</b></dt>
</dl>
</td>
<td width="60%">
The counter path string could not be parsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate a required temporary buffer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f2dc5f77-9f9e-4290-95fa-ce2f1e81fc69">PdhMakeCounterPath</a>



<a href="https://msdn.microsoft.com/9248e63c-2672-466f-85f5-46f26e31dc75">PdhValidatePath</a>
 

 

