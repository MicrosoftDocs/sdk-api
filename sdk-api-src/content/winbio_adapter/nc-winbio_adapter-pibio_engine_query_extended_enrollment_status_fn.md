---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN
title: PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN
author: windows-sdk-content
description: Queries the WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS property.
old-location: secbiomet\engineadapterqueryextendedenrollmentstatus.htm
old-project: secbiomet
ms.assetid: E471FC60-9FFC-4269-92A0-7CCA53D3475B
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: EngineAdapterQueryExtendedEnrollmentStatus, EngineAdapterQueryExtendedEnrollmentStatus callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN, PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN callback, secbiomet.engineadapterqueryextendedenrollmentstatus, winbio_adapter/EngineAdapterQueryExtendedEnrollmentStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.redist: 
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
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterQueryExtendedEnrollmentStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN callback function


## -description


Called by the Windows Biometric Framework when a client application queries the <b>WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS</b>  property.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param EnrollmentStatus [out]

Pointer to the <a href="https://msdn.microsoft.com/2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B">WINBIO_EXTENDED_ENROLLMENT_STATUS</a> structure that contains the extended enrollment status information returned by this function.


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



Enrollment applications can request extended enrollment status information after each call to the <a href="https://msdn.microsoft.com/a50f0c9f-7b9c-4d80-b8fc-8b83bc333578">WinBioEnrollCapture</a> function.

If the biometric unit is not currently an enrollment template when this routine is called, the engine adapter should set the EnrollmentStatus.TemplateStatus field to <b>WINBIO_E_INVALID_OPERATION</b> and return <b>S_OK</b> as the value of the function.



