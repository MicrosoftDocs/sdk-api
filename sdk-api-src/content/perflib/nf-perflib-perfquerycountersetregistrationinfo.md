---
UID: NF:perflib.PerfQueryCounterSetRegistrationInfo
title: PerfQueryCounterSetRegistrationInfo function (perflib.h)
description: Gets information about a counter set on the specified system.
helpviewer_keywords: ["PerfQueryCounterSetRegistrationInfo","PerfQueryCounterSetRegistrationInfo function [Perf]","perf.perfquerycountersetregistrationinfo","perflib/PerfQueryCounterSetRegistrationInfo"]
old-location: perf\perfquerycountersetregistrationinfo.htm
tech.root: perf
ms.assetid: E8E83E47-2445-42AE-855F-6710FC8F789E
ms.date: 12/05/2018
ms.keywords: PerfQueryCounterSetRegistrationInfo, PerfQueryCounterSetRegistrationInfo function [Perf], perf.perfquerycountersetregistrationinfo, perflib/PerfQueryCounterSetRegistrationInfo
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
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PerfQueryCounterSetRegistrationInfo
 - perflib/PerfQueryCounterSetRegistrationInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - AdvAPI32.dll
 - api-ms-win-perf-legacy-l1-1-0.dll
api_name:
 - PerfQueryCounterSetRegistrationInfo
---

# PerfQueryCounterSetRegistrationInfo function


## -description

Gets information about a counter set on the specified system.

## -parameters

### -param szMachine [in, optional]

The name of the machine for which to get the information about the counter set  that the <i>pCounterSet</i> parameter specifies. If NULL, the function retrieves information about the specified counter set for the local machine.

### -param pCounterSetId [in]

The counter set identifier of the counter set for which you want to get information.

### -param requestCode

The type of information that you want to get about the counter set. See <a href="/windows/desktop/api/perflib/ne-perflib-perfreginfotype">PerfRegInfoType</a> for a list of possible values.

### -param requestLangId

The preferred locale identifier for the strings that contain the requested information if <i>requestCode</i> is <b>PERF_REG_COUNTERSET_NAME_STRING</b>,  

<b>PERF_REG_COUNTERSET_HELP_STRING</b>, <b>PERF_REG_COUNTER_NAME_STRINGS</b>, or  

<b>PERF_REG_COUNTER_HELP_STRINGS</b>.

The counter identifier of the counter for which you want data, if <i>requestCode</i> is <b>PERF_REG_COUNTER_STRUCT</b>. 

Set to 0 for all other values of <i>requestCode</i>.

### -param pbRegInfo [out, optional]

Pointer to a buffer that is large enough to receive the amount of data that the <i>cbRegInfo</i> parameter specifies, in bytes. May be  

NULL if <i>cbRegInfo</i> is 0.

### -param cbRegInfo

The size of the buffer that the <i>pbRegInfo</i> parameter specifies, in bytes.

### -param pcbRegInfoActual [out]

The size of the buffer actually required to get the information about the counter set. The meaning depends on the value that the function  

returns.

<table>
<tr>
<th>Function  Return Value</th>
<th>Meaning of <i>pcbRegInfoActual</i></th>
</tr>
<tr>
<td><b>ERROR_SUCCESS</b></td>
<td>The number of  

  bytes of information about the specified counter set that the function stored in the buffer that <i>pbRegInfo</i> specified.</td>
</tr>
<tr>
<td><b> ERROR_NOT_ENOUGH_MEMORY</b></td>
<td>The  

  size of the buffer required to store the information about the counter set on the specified machine, in bytes. Enlarge the buffer to the required  

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
The function successfully stored all of the information about the counter set in the buffer that <i>pbRegInfo</i> specified. The value that <i>pcbRegInfoActual</i> points to indicates amount of information actually stored in the buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
 The buffer that <i>pbRegInfo</i> specified was not large enough to store all of the information about the counter set.  The value that <i>pcbRegInfoActual</i> points to  indicates the size of the buffer required to store all of the information. Enlarge the buffer to the required  

  size and call the function again.  



</td>
</tr>
</table>
 

For other types of failures, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

See  <a href="/windows/desktop/api/perflib/ne-perflib-perfreginfotype">PerfRegInfoType</a>  for the types of data that you can request and  

the formats of the data provided for each type of request.