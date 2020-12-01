---
UID: NS:winbase._OPERATION_END_PARAMETERS
title: OPERATION_END_PARAMETERS (winbase.h)
description: This structure is used by the OperationEnd function.
helpviewer_keywords: ["*POPERATION_END_PARAMETERS","OPERATION_API_VERSION","OPERATION_END_DISCARD","OPERATION_END_PARAMETERS","OPERATION_END_PARAMETERS structure [Operation Recorder]","POPERATION_END_PARAMETERS","POPERATION_END_PARAMETERS structure pointer [Operation Recorder]","_OPERATION_END_PARAMETERS","oprec.operation_end_parameters","winbase/OPERATION_END_PARAMETERS","winbase/POPERATION_END_PARAMETERS"]
old-location: oprec\operation_end_parameters.htm
tech.root: oprec
ms.assetid: 45ABFE6A-7B70-418F-8C3C-6388079D1306
ms.date: 12/05/2018
ms.keywords: '*POPERATION_END_PARAMETERS, OPERATION_API_VERSION, OPERATION_END_DISCARD, OPERATION_END_PARAMETERS, OPERATION_END_PARAMETERS structure [Operation Recorder], POPERATION_END_PARAMETERS, POPERATION_END_PARAMETERS structure pointer [Operation Recorder], _OPERATION_END_PARAMETERS, oprec.operation_end_parameters, winbase/OPERATION_END_PARAMETERS, winbase/POPERATION_END_PARAMETERS'
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
req.typenames: OPERATION_END_PARAMETERS, *POPERATION_END_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPERATION_END_PARAMETERS
 - winbase/_OPERATION_END_PARAMETERS
 - POPERATION_END_PARAMETERS
 - winbase/POPERATION_END_PARAMETERS
 - OPERATION_END_PARAMETERS
 - winbase/OPERATION_END_PARAMETERS
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
 - OPERATION_END_PARAMETERS
---

# OPERATION_END_PARAMETERS structure


## -description

This structure is used by the <a href="/windows/desktop/api/winbase/nf-winbase-operationend">OperationEnd</a> function.

## -struct-fields

### -field Version

This parameter should be initialized to the  <b>OPERATION_API_VERSION</b> defined in the Windows SDK. 

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
<td width="40%"><a id="OPERATION_END_DISCARD"></a><a id="operation_end_discard"></a><dl>
<dt><b>OPERATION_END_DISCARD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Specifies that the system should discard the information it has been tracking for this operation. Specify this flag when the operation either fails or does not follow the expected sequence of steps. 

</td>
</tr>
</table>

## -see-also

<b></b>



<a href="/previous-versions/windows/desktop/oprec/operation-id">OPERATION_ID</a>



<a href="/windows/desktop/api/winbase/ns-winbase-operation_start_parameters">OPERATION_START_PARAMETERS</a>



<a href="/previous-versions/windows/desktop/oprec/-operation-portal">Operation Recorder</a>



<a href="/windows/desktop/api/winbase/nf-winbase-operationend">OperationEnd</a>



<a href="/windows/desktop/api/winbase/nf-winbase-operationstart">OperationStart</a>