---
UID: NS:winbase._OPERATION_START_PARAMETERS
title: OPERATION_START_PARAMETERS (winbase.h)
description: This structure is used by the OperationStart function.
helpviewer_keywords: ["*POPERATION_START_PARAMETERS","OPERATION_API_VERSION","OPERATION_START_PARAMETERS","OPERATION_START_PARAMETERS structure [Operation Recorder]","OPERATION_START_TRACE_CURRENT_THREAD","POPERATION_START_PARAMETERS","POPERATION_START_PARAMETERS structure pointer [Operation Recorder]","_OPERATION_START_PARAMETERS","oprec.operation_start_parameters","winbase/OPERATION_START_PARAMETERS","winbase/POPERATION_START_PARAMETERS"]
old-location: oprec\operation_start_parameters.htm
tech.root: oprec
ms.assetid: 51AE0017-2CDE-4BCD-AE03-B366343DE558
ms.date: 12/05/2018
ms.keywords: '*POPERATION_START_PARAMETERS, OPERATION_API_VERSION, OPERATION_START_PARAMETERS, OPERATION_START_PARAMETERS structure [Operation Recorder], OPERATION_START_TRACE_CURRENT_THREAD, POPERATION_START_PARAMETERS, POPERATION_START_PARAMETERS structure pointer [Operation Recorder], _OPERATION_START_PARAMETERS, oprec.operation_start_parameters, winbase/OPERATION_START_PARAMETERS, winbase/POPERATION_START_PARAMETERS'
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPERATION_START_PARAMETERS, *POPERATION_START_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPERATION_START_PARAMETERS
 - winbase/_OPERATION_START_PARAMETERS
 - POPERATION_START_PARAMETERS
 - winbase/POPERATION_START_PARAMETERS
 - OPERATION_START_PARAMETERS
 - winbase/OPERATION_START_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - OPERATION_START_PARAMETERS
---

# OPERATION_START_PARAMETERS structure


## -description

This structure is used by the <a href="/windows/desktop/api/winbase/nf-winbase-operationstart">OperationStart</a> function.

## -struct-fields

### -field Version

This parameter should be initialized to the  <b>OPERATION_API_VERSION</b> value defined in the Windows SDK. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPERATION_API_VERSION"></a><a id="operation_api_version"></a><dl>
<dt><b>OPERATION_API_VERSION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
This API was introduced in Windows 8 and Windows Server 2012 as version 1.

</td>
</tr>
</table>

### -field OperationId

Each operation has an <a href="/previous-versions/windows/desktop/oprec/operation-id">OPERATION_ID</a> namespace that is unique for each process. If two applications both use the same <b>OPERATION_ID</b> value to identify two operations, the system maintains separate contexts for each operation.

### -field Flags

The value of this parameter can include any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPERATION_START_TRACE_CURRENT_THREAD"></a><a id="operation_start_trace_current_thread"></a><dl>
<dt><b>OPERATION_START_TRACE_CURRENT_THREAD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Specifies that the system should only track the activities of the calling thread in a multi-threaded application. Specify this flag when the operation is performed on a single thread to isolate its activity from other threads in the process.  

</td>
</tr>
</table>

## -see-also

<b></b>



<a href="/windows/desktop/api/winbase/ns-winbase-operation_end_parameters">OPERATION_END_PARAMETERS</a>



<a href="/previous-versions/windows/desktop/oprec/operation-id">OPERATION_ID</a>



<a href="/previous-versions/windows/desktop/oprec/-operation-portal">Operation Recorder</a>



<a href="/windows/desktop/api/winbase/nf-winbase-operationend">OperationEnd </a>



<a href="/windows/desktop/api/winbase/nf-winbase-operationstart">OperationStart</a>