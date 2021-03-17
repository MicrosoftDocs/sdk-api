---
UID: NC:winbio_adapter.PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN
title: PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN (winbio_adapter.h)
description: Tells the Engine Adapter which person to track for the current enrollment operation.
helpviewer_keywords: ["EngineAdapterSetEnrollmentSelector","EngineAdapterSetEnrollmentSelector callback function [Windows Biometric Framework API]","PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN","PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN callback","secbiomet.engineadaptersetenrollmentselector","winbio_adapter/EngineAdapterSetEnrollmentSelector"]
old-location: secbiomet\engineadaptersetenrollmentselector.htm
tech.root: SecBioMet
ms.assetid: 4374F4BA-2B09-4C89-9B5E-CF6B53220A4F
ms.date: 12/05/2018
ms.keywords: EngineAdapterSetEnrollmentSelector, EngineAdapterSetEnrollmentSelector callback function [Windows Biometric Framework API], PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN, PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN callback, secbiomet.engineadaptersetenrollmentselector, winbio_adapter/EngineAdapterSetEnrollmentSelector
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
 - PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN
 - winbio_adapter/PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN
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
 - EngineAdapterSetEnrollmentSelector
---

# PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN callback function


## -description

Called by the Windows Biometric Framework to tell the Engine Adapter which person to track for the current enrollment operation.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

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

For some biometric factors (such as WINBIO_TYPE_FACIAL_FEATURES), there can be multiple people in camera frame at the same time. During an enrollment operation, it’s necessary for the enrollment application to select one specific person to enroll. The enrollment application does this by calling the <a href="/windows/desktop/api/winbio/nf-winbio-winbioenrollselect">WinBioEnrollSelect</a> function. The Windows Biometric Framework then calls the engine adapter’s <b>EngineAdapterSetEnrollmentSelector</b> function with this information.

The engine adapter should store this value and use it to track the proper person during the course of the enrollment.