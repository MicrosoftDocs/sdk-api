---
UID: NC:winbio_adapter.PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN
title: PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN
author: windows-sdk-content
description: Gives the engine adapter additional information about an enrollment operation.
old-location: secbiomet\engineadaptersetenrollmentparameters.htm
tech.root: SecBioMet
ms.assetid: BB353505-F861-47BD-A617-42F0AA39251E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EngineAdapterSetEnrollmentParameters, EngineAdapterSetEnrollmentParameters callback function [Windows Biometric Framework API], PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN, PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN callback, secbiomet.engineadaptersetenrollmentparameters, winbio_adapter/EngineAdapterSetEnrollmentParameters
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterSetEnrollmentParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN callback function


## -description


Called by the Windows Biometric Framework to give the engine adapter additional information about an enrollment operation.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param Parameters [in]

Pointer to the <a href="https://msdn.microsoft.com/E8007316-0A9D-4F35-A266-273B2406D545">WINBIO_EXTENDED_ENROLLMENT_PARAMETERS</a> structure containing the extended enrollment parameters to use.


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
</table>
 




## -remarks



If the engine adapter successfully completes an <a href="https://msdn.microsoft.com/5eec81ec-490c-485f-bbaf-4d972d7c8fde">EngineAdapterCreateEnrollment</a> call, it will immediately receive a call to its <b>EngineAdapterSetEnrollmentParameters</b> function.

 This function specifies the subfactor to be used for the new enrollment template.



