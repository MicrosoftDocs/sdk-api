---
UID: NF:objbase.CoDosDateTimeToFileTime
title: CoDosDateTimeToFileTime function (objbase.h)
description: Converts the MS-DOS representation of the time and date to a FILETIME structure used by Windows.
helpviewer_keywords: ["CoDosDateTimeToFileTime","CoDosDateTimeToFileTime function [COM]","_com_CoDosDateTimeToFileTime","com.codosdatetimetofiletime","objbase/CoDosDateTimeToFileTime"]
old-location: com\codosdatetimetofiletime.htm
tech.root: com
ms.assetid: eb7af6a3-7547-405e-b96e-3e68a1ac273b
ms.date: 12/05/2018
ms.keywords: CoDosDateTimeToFileTime, CoDosDateTimeToFileTime function [COM], _com_CoDosDateTimeToFileTime, com.codosdatetimetofiletime, objbase/CoDosDateTimeToFileTime
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoDosDateTimeToFileTime
 - objbase/CoDosDateTimeToFileTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
api_name:
 - CoDosDateTimeToFileTime
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# CoDosDateTimeToFileTime function


## -description

Converts the MS-DOS representation of the time and date to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure used by Windows.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters

### -param nDosDate [in]

The MS-DOS date.

### -param nDosTime [in]

The MS-DOS time.

### -param lpFileTime [out]

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>; otherwise, it is <b>FALSE</b>, probably because of invalid arguments.

## -remarks

 An MS-DOS date has the following format.

<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0-4</td>
<td>Days of the month (1-31).
</td>
</tr>
<tr>
<td>5-8</td>
<td>Months (1 = January, 2 = February, and so forth). 
</td>
</tr>
<tr>
<td>9-15</td>
<td>Year offset from 1980 (add 1980 to get actual year). 
</td>
</tr>
</table>
 

An MS-DOS time has the following format.

<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0-4</td>
<td>Seconds divided by 2.</td>
</tr>
<tr>
<td>5-10</td>
<td>Minutes (0-59).
</td>
</tr>
<tr>
<td>11-15</td>
<td>Hours (0-23 on a 24-hour clock). 
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofiletimenow">CoFileTimeNow</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cofiletimetodosdatetime">CoFileTimeToDosDateTime</a>
