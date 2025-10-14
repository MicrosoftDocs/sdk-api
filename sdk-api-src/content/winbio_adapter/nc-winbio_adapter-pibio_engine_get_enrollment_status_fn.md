---
UID: NC:winbio_adapter.PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN
title: PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN (winbio_adapter.h)
description: Determines whether the enrollment object is ready to be committed to the pipeline.
helpviewer_keywords: ["EngineAdapterGetEnrollmentStatus","EngineAdapterGetEnrollmentStatus callback function [Windows Biometric Framework API]","PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN","PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN callback","secbiomet.engineadaptergetenrollmentstatus","winbio_adapter/EngineAdapterGetEnrollmentStatus"]
old-location: secbiomet\engineadaptergetenrollmentstatus.htm
tech.root: SecBioMet
ms.assetid: cd029d7e-e103-4bbb-aaf9-36f3043b941c
ms.date: 12/05/2018
ms.keywords: EngineAdapterGetEnrollmentStatus, EngineAdapterGetEnrollmentStatus callback function [Windows Biometric Framework API], PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN, PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN callback, secbiomet.engineadaptergetenrollmentstatus, winbio_adapter/EngineAdapterGetEnrollmentStatus
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN
 - winbio_adapter/PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterGetEnrollmentStatus
---

# PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN callback function


## -description

Called by the Windows Biometric Framework to determine whether the enrollment object is ready to be committed to the pipeline.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param RejectDetail [out]

A pointer to a <b>WINBIO_REJECT_DETAIL</b> value that receives additional information about the failure to update the enrollment object. If the last update was successful, you should set this variable to zero.

## -returns

This function must return one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The last update succeeded and no additional feature sets are required to complete the template.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> WINBIO_E_BAD_CAPTURE</b></dt>
</dl>
</td>
<td width="60%">
The feature set did not meet the internal enrollment requirements of the engine adapter. Further information about the failure is specified by the <i>RejectDetail</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
There is no enrollment in progress on this biometric unit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_I_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The last update succeeded, but the engine adapter requires one or more additional feature sets before it can complete the enrollment template.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn">EngineAdapterUpdateEnrollment</a>



<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>