---
UID: NF:pdh.PdhValidatePathA
title: PdhValidatePathA function (pdh.h)
author: windows-sdk-content
description: Validates that the counter is present on the computer specified in the counter path.
old-location: perf\pdhvalidatepath.htm
tech.root: perfctrs
ms.assetid: 9248e63c-2672-466f-85f5-46f26e31dc75
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PdhValidatePath, PdhValidatePath function [Perf], PdhValidatePathA, PdhValidatePathW, _win32_pdhvalidatepath, base.pdhvalidatepath, pdh/PdhValidatePath, pdh/PdhValidatePathA, pdh/PdhValidatePathW, perf.pdhvalidatepath
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhValidatePathW (Unicode) and PdhValidatePathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhValidatePath
 - PdhValidatePathA
 - PdhValidatePathW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdhValidatePathA function


## -description


Validates that the counter is present on the computer specified in the counter path.
		


## -parameters




### -param szFullPathBuffer [in]

Null-terminated string that contains the counter path to validate. The maximum length of a counter path is PDH_MAX_COUNTER_PATH.


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
The specified performance object was not found on the computer.

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
 

 

