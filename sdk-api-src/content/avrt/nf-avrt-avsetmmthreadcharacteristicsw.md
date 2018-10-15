---
UID: NF:avrt.AvSetMmThreadCharacteristicsW
title: AvSetMmThreadCharacteristicsW function
author: windows-sdk-content
description: Associates the calling thread with the specified task.
old-location: base\avsetmmthreadcharacteristics.htm
tech.root: ProcThread
ms.assetid: 881d3f97-e68e-40cb-b799-76784185dd37
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AvSetMmThreadCharacteristics, AvSetMmThreadCharacteristics function, AvSetMmThreadCharacteristicsA, AvSetMmThreadCharacteristicsW, avrt/AvSetMmThreadCharacteristics, avrt/AvSetMmThreadCharacteristicsA, avrt/AvSetMmThreadCharacteristicsW, base.avsetmmthreadcharacteristics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: avrt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AvSetMmThreadCharacteristicsW (Unicode) and AvSetMmThreadCharacteristicsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvSetMmThreadCharacteristics
 - AvSetMmThreadCharacteristicsA
 - AvSetMmThreadCharacteristicsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AvSetMmThreadCharacteristicsW function


## -description


Associates the calling thread with the specified task.


## -parameters




### -param TaskName [in]

The name of the task to be performed. This name must match the name of one of the subkeys of the following key <b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks</b>.


### -param TaskIndex [in, out]

The unique task identifier. The first time this function is called, this value must be 0 on input. The index value is returned on output and can be used as input in subsequent calls.


## -returns



If the function succeeds, it returns a handle to the task. 

If the function fails, it returns 0. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


The following are possible error codes.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_TASK_INDEX</b></dt>
</dl>
</td>
<td width="60%">
Either <i>TaskIndex</i> is not 0 on the first call or is not recognized value (on subsequent calls).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_TASK_NAME</b></dt>
</dl>
</td>
<td width="60%">
The specified task does not match any of the tasks stored in the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PRIVILEGE_NOT_HELD</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privilege.

</td>
</tr>
</table>
 




## -remarks



When the task is completed, call the <a href="https://msdn.microsoft.com/2ae0d34c-3819-46fa-9779-5de8a57e5281">AvRevertMmThreadCharacteristics</a> function.




## -see-also




<a href="https://msdn.microsoft.com/a7169938-1c72-4c4c-881a-cb08ad6182c7">Multimedia Class Scheduler Service</a>
 

 

