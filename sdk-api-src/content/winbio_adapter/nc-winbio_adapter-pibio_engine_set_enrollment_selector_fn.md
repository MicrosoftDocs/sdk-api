---
UID: NC:winbio_adapter.PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN
title: PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN
author: windows-sdk-content
description: Tells the Engine Adapter which person to track for the current enrollment operation.
old-location: secbiomet\engineadaptersetenrollmentselector.htm
old-project: SecBioMet
ms.assetid: 4374F4BA-2B09-4C89-9B5E-CF6B53220A4F
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: EngineAdapterSetEnrollmentSelector, EngineAdapterSetEnrollmentSelector callback function [Windows Biometric Framework API], PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN, PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN callback, secbiomet.engineadaptersetenrollmentselector, winbio_adapter/EngineAdapterSetEnrollmentSelector
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	EngineAdapterSetEnrollmentSelector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN callback function


## -description


Called by the Windows Biometric Framework to tell the Engine Adapter which person to track for the current enrollment operation.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param SelectorValue [in]

The enrollment selector value to use.


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



For some biometric factors (such as WINBIO_TYPE_FACIAL_FEATURES), there can be multiple people in camera frame at the same time. During an enrollment operation, it’s necessary for the enrollment application to select one specific person to enroll. The enrollment application does this by calling the <a href="https://msdn.microsoft.com/9C06B976-9B60-43B6-B68B-255A6882912B">WinBioEnrollSelect</a> function. The Windows Biometric Framework then calls the engine adapter’s <b>EngineAdapterSetEnrollmentSelector</b> function with this information.

The engine adapter should store this value and use it to track the proper person during the course of the enrollment.



