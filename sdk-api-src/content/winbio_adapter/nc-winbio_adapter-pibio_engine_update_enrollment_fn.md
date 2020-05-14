---
UID: NC:winbio_adapter.PIBIO_ENGINE_UPDATE_ENROLLMENT_FN
title: PIBIO_ENGINE_UPDATE_ENROLLMENT_FN (winbio_adapter.h)
description: Adds the current feature set to the enrollment object.helpviewer_keywords: ["EngineAdapterUpdateEnrollment","EngineAdapterUpdateEnrollment callback function [Windows Biometric Framework API]","PIBIO_ENGINE_UPDATE_ENROLLMENT_FN","PIBIO_ENGINE_UPDATE_ENROLLMENT_FN callback","secbiomet.engineadapterupdateenrollment","winbio_adapter/EngineAdapterUpdateEnrollment"]
old-location: secbiomet\engineadapterupdateenrollment.htm
tech.root: SecBioMet
ms.assetid: cd41be8c-fa78-4746-a9ad-c8385ed84b52
ms.date: 12/05/2018
ms.keywords: EngineAdapterUpdateEnrollment, EngineAdapterUpdateEnrollment callback function [Windows Biometric Framework API], PIBIO_ENGINE_UPDATE_ENROLLMENT_FN, PIBIO_ENGINE_UPDATE_ENROLLMENT_FN callback, secbiomet.engineadapterupdateenrollment, winbio_adapter/EngineAdapterUpdateEnrollment
f1_keywords:
- winbio_adapter/EngineAdapterUpdateEnrollment
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Winbio_adapter.h
api_name:
- EngineAdapterUpdateEnrollment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_ENGINE_UPDATE_ENROLLMENT_FN callback function


## -description


Called by the Windows Biometric Framework to add the current feature set to the enrollment object.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param RejectDetail [out]

Pointer to a <b>WINBIO_REJECT_DETAIL</b> value that receives  additional information about the failure to update the enrollment object. If the update succeeds, this value should be set to zero.


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
<dt><b><b> WINBIO_E_BAD_CAPTURE</b></b></dt>
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
<dt><b><b>WINBIO_I_MORE_DATA</b></b></dt>
</dl>
</td>
<td width="60%">
The last update succeeded, but the engine adapter requires one or more additional feature sets before it can complete the enrollment template.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn">EngineAdapterGetEnrollmentStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>
 

 

