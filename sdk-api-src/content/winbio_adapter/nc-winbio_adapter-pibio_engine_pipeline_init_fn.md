---
UID: NC:winbio_adapter.PIBIO_ENGINE_PIPELINE_INIT_FN
title: PIBIO_ENGINE_PIPELINE_INIT_FN (winbio_adapter.h)
author: windows-sdk-content
description: Gives the Engine Adapter the chance to perform any initialization that remains incomplete.
old-location: secbiomet\engineadapterpipelineinit.htm
tech.root: SecBioMet
ms.assetid: 69D4BB35-2E00-4FF6-8A69-DFCEFA5785A0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngineAdapterPipelineInit, EngineAdapterPipelineInit callback function [Windows Biometric Framework API], PIBIO_ENGINE_PIPELINE_INIT_FN, PIBIO_ENGINE_PIPELINE_INIT_FN callback, secbiomet.engineadapterpipelineinit, winbio_adapter/EngineAdapterPipelineInit
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
 - EngineAdapterPipelineInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_ENGINE_PIPELINE_INIT_FN callback function


## -description


Called by the Windows Biometric Framework to give the Engine Adapter the chance to perform any initialization that remains incomplete.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


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
<dt><b>E_some_error </b></dt>
</dl>
</td>
<td width="60%">
Any error code will cause the Biometric Service to log the error and abort the configuration of the biometric unit.

</td>
</tr>
</table>
 




## -remarks



The Engine Adapter should return <b>S_OK</b> if it doesn’t need to perform any initialization at this point.

When this routine is called, the <a href="https://msdn.microsoft.com/91243128-0543-4df9-bde8-74ef5ae46914">SensorAdapterAttach</a>, <a href="https://msdn.microsoft.com/e797952b-c7dd-41ad-9536-97d7ce1a7a5d">EngineAdapterAttach</a>, and,<a href="https://msdn.microsoft.com/6abded6b-12e0-4cc6-a011-0b18e8ea747b">StorageAdapterAttach</a> routines have completed normally, the template database is open, and the <a href="https://msdn.microsoft.com/F969AC5A-6760-4904-A04E-F2FEF4290F7A">StorageAdapterPipelineInit</a> routine has completed normally.

This method executes in the context of an arbitrary RPC server thread.



