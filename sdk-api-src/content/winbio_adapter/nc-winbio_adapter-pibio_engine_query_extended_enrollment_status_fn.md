---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN
title: PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN (winbio_adapter.h)
description: Queries the WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS property.
helpviewer_keywords: ["EngineAdapterQueryExtendedEnrollmentStatus","EngineAdapterQueryExtendedEnrollmentStatus callback function [Windows Biometric Framework API]","PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN","PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN callback","secbiomet.engineadapterqueryextendedenrollmentstatus","winbio_adapter/EngineAdapterQueryExtendedEnrollmentStatus"]
old-location: secbiomet\engineadapterqueryextendedenrollmentstatus.htm
tech.root: SecBioMet
ms.assetid: E471FC60-9FFC-4269-92A0-7CCA53D3475B
ms.date: 12/05/2018
ms.keywords: EngineAdapterQueryExtendedEnrollmentStatus, EngineAdapterQueryExtendedEnrollmentStatus callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN, PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN callback, secbiomet.engineadapterqueryextendedenrollmentstatus, winbio_adapter/EngineAdapterQueryExtendedEnrollmentStatus
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN
 - winbio_adapter/PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN
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
 - EngineAdapterQueryExtendedEnrollmentStatus
---

# PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN callback function


## -description

Called by the Windows Biometric Framework when a client application queries the <b>WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS</b>  property.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param EnrollmentStatus [out]

Pointer to the <a href="/windows/desktop/SecBioMet/winbio-extended-enrollment-status">WINBIO_EXTENDED_ENROLLMENT_STATUS</a> structure that contains the extended enrollment status information returned by this function.

### -param EnrollmentStatusSize [in]

The specified size in bytes of the extended enrollment status information.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The <i>EnrollmentStatusSize</i> parameter indicates that the output buffer is too small.

</td>
</tr>
</table>

## -remarks

Enrollment applications can request extended enrollment status information after each call to the <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollcapture">WinBioEnrollCapture</a> function.

If the biometric unit is not currently an enrollment template when this routine is called, the engine adapter should set the EnrollmentStatus.TemplateStatus field to <b>WINBIO_E_INVALID_OPERATION</b> and return <b>S_OK</b> as the value of the function.