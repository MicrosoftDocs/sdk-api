---
UID: NF:avrt.AvSetMmMaxThreadCharacteristicsW
title: AvSetMmMaxThreadCharacteristicsW function (avrt.h)
description: Associates the calling thread with the specified tasks. (Unicode)
helpviewer_keywords: ["AvSetMmMaxThreadCharacteristics", "AvSetMmMaxThreadCharacteristics function", "AvSetMmMaxThreadCharacteristicsW", "avrt/AvSetMmMaxThreadCharacteristics", "avrt/AvSetMmMaxThreadCharacteristicsW", "base.avsetmmmaxthreadcharacteristics"]
old-location: base\avsetmmmaxthreadcharacteristics.htm
tech.root: backup
ms.assetid: d8137b53-b1fd-4c25-909a-d0ed671848df
ms.date: 12/05/2018
ms.keywords: AvSetMmMaxThreadCharacteristics, AvSetMmMaxThreadCharacteristics function, AvSetMmMaxThreadCharacteristicsA, AvSetMmMaxThreadCharacteristicsW, avrt/AvSetMmMaxThreadCharacteristics, avrt/AvSetMmMaxThreadCharacteristicsA, avrt/AvSetMmMaxThreadCharacteristicsW, base.avsetmmmaxthreadcharacteristics
req.header: avrt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AvSetMmMaxThreadCharacteristicsW (Unicode) and AvSetMmMaxThreadCharacteristicsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AvSetMmMaxThreadCharacteristicsW
 - avrt/AvSetMmMaxThreadCharacteristicsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvSetMmMaxThreadCharacteristics
 - AvSetMmMaxThreadCharacteristicsA
 - AvSetMmMaxThreadCharacteristicsW
---

# AvSetMmMaxThreadCharacteristicsW function


## -description

Associates the calling thread with the specified tasks.

## -parameters

### -param FirstTask [in]

The name of the first task to be performed. This name must match the name of one of the subkeys of the following key <b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks</b>.

### -param SecondTask [in]

The name of the second task to be performed. This name must match the name of one of the subkeys of the following key <b>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks</b>.

### -param TaskIndex [in, out]

The unique task identifier. The first time this function is called, this value must be 0 on input. The index value is returned on output and can be used as input in subsequent calls.

## -returns

If the function succeeds, it returns a handle to the task. 

If the function fails, it returns 0. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


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

The resulting characteristics of the thread performing the tasks reflect the task with the highest priority.

When the task is completed, call the <a href="/windows/desktop/api/avrt/nf-avrt-avrevertmmthreadcharacteristics">AvRevertMmThreadCharacteristics</a> function.





> [!NOTE]
> The avrt.h header defines AvSetMmMaxThreadCharacteristics as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/ProcThread/multimedia-class-scheduler-service">Multimedia Class Scheduler Service</a>
