---
UID: NC:winbio_adapter.PIBIO_ENGINE_PIPELINE_CLEANUP_FN
title: PIBIO_ENGINE_PIPELINE_CLEANUP_FN
author: windows-sdk-content
description: Gives the Engine Adapter the chance to perform any cleanup that requires help from the Storage Adapter.
old-location: secbiomet\engineadapterpipelinecleanup.htm
tech.root: SecBioMet
ms.assetid: C77EBE33-E781-4FFA-BE3A-A08BD9C3D459
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EngineAdapterPipelineCleanup, EngineAdapterPipelineCleanup callback function [Windows Biometric Framework API], PIBIO_ENGINE_PIPELINE_CLEANUP_FN, PIBIO_ENGINE_PIPELINE_CLEANUP_FN callback, secbiomet.engineadapterpipelinecleanup, winbio_adapter/EngineAdapterPipelineCleanup
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
 - EngineAdapterPipelineCleanup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_ENGINE_PIPELINE_CLEANUP_FN callback function


## -description


Called by the Windows Biometric Framework to give the Engine Adapter the chance to perform any cleanup that requires help from the Storage Adapter.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method is called once, when a biometric unit is being torn down.

The Engine Adapter should return <b>S_OK</b> if it doesn’t need to perform any cleanup at this point.

This method executes in the context of an arbitrary RPC server thread.



