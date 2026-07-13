---
UID: NF:perflib.PerfEnumerateCounterSet
title: PerfEnumerateCounterSet function (perflib.h)
description: Gets the counter set identifiers of the counter sets that are registered on the specified system. Counter set identifiers are globally unique identifiers (GUIDs).
helpviewer_keywords: ["PerfEnumerateCounterSet","PerfEnumerateCounterSet function [Perf]","perf.perfenumeratecounterset","perflib/PerfEnumerateCounterSet"]
old-location: perf\perfenumeratecounterset.htm
tech.root: perf
ms.assetid: 6C487D11-2DC0-475C-AA0F-4060641C6500
ms.date: 12/05/2018
ms.keywords: PerfEnumerateCounterSet, PerfEnumerateCounterSet function [Perf], perf.perfenumeratecounterset, perflib/PerfEnumerateCounterSet
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
 - PerfEnumerateCounterSet
 - perflib/PerfEnumerateCounterSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-perf-legacy-l1-1-0.dll
 - AdvAPI32.dll
api_name:
 - PerfEnumerateCounterSet
---

# PerfEnumerateCounterSet function


## -description

Gets the counter set identifiers of the counter sets that are registered on the  

specified system.  

Counter set identifiers are globally unique identifiers (GUIDs).

## -parameters

### -param szMachine [in, optional]

The name of the machine for which to get the counter set identifiers. If NULL, the function retrieves the counter set identifiers for the local machine.

### -param pCounterSetIds [out, optional]

A pointer to a buffer that has enough space to receive the number of GUIDs that the <i>cCounterSetIds</i> parameter specifies. May be NULL if  

<i>cCounterSetIds</i> is 0.

### -param cCounterSetIds

The size of the buffer that the <i>pCounterSetIds</i> parameter specifies, measured in GUIDs.

### -param pcCounterSetIdsActual [out]

The size of the buffer actually required to get the counter set identifiers. The meaning depends on the value that the function  

returns.

<table>
<tr>
<th>Function  Return Value</th>
<th>Meaning of <i>pcCounterSetIdsActual</i></th>
</tr>
<tr>
<td><b>ERROR_SUCCESS</b></td>
<td>The number of  

  GUIDs that the function stored in the buffer that <i>pCounterSetIds</i> specified.</td>
</tr>
<tr>
<td><b> ERROR_NOT_ENOUGH_MEMORY</b></td>
<td>The  

  size (in GUIDs) of the buffer required. Enlarge the buffer to the required  

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
The function successfully stored all of the content set identifiers in the buffer that <i>pCounterSetIds</i> specified. The value that <i>pcCounterSetIdsActual</i> points to indicates the number of counter set identifiers actually stored in the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
 The buffer that <i>pCounterSetIds</i> specified was not large enough to store all of the counter set identifiers for the counter sets on the specified system.  The value that <i>pcCounterSetIdsActual</i> points to  indicates the size of the buffer required to store all of the counter set identifiers. Enlarge the buffer to the required  

  size and call the function again.  



</td>
</tr>
</table>
 

For other types of failures, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfenumeratecountersetinstances">PerfEnumerateCounterSetInstances</a>