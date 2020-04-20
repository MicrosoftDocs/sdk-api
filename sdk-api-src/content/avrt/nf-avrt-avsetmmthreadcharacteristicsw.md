---
UID: NF:avrt.AvSetMmThreadCharacteristicsW
title: AvSetMmThreadCharacteristicsW function (avrt.h)
description: Associates the calling thread with the specified task.helpviewer_keywords: ["AvSetMmThreadCharacteristics","AvSetMmThreadCharacteristics function","AvSetMmThreadCharacteristicsA","AvSetMmThreadCharacteristicsW","avrt/AvSetMmThreadCharacteristics","avrt/AvSetMmThreadCharacteristicsA","avrt/AvSetMmThreadCharacteristicsW","base.avsetmmthreadcharacteristics"]
old-location: base\avsetmmthreadcharacteristics.htm
tech.root: ProcThread
ms.assetid: 881d3f97-e68e-40cb-b799-76784185dd37
ms.date: 12/05/2018
ms.keywords: AvSetMmThreadCharacteristics, AvSetMmThreadCharacteristics function, AvSetMmThreadCharacteristicsA, AvSetMmThreadCharacteristicsW, avrt/AvSetMmThreadCharacteristics, avrt/AvSetMmThreadCharacteristicsA, avrt/AvSetMmThreadCharacteristicsW, base.avsetmmthreadcharacteristics
f1_keywords:
- avrt/AvSetMmThreadCharacteristics
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

If the function fails, it returns 0. To retrieve extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


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



When the task is completed, call the <a href="https://docs.microsoft.com/windows/desktop/api/avrt/nf-avrt-avrevertmmthreadcharacteristics">AvRevertMmThreadCharacteristics</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/multimedia-class-scheduler-service">Multimedia Class Scheduler Service</a>
 

 

