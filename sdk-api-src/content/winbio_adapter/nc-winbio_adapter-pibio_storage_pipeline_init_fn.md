---
UID: NC:winbio_adapter.PIBIO_STORAGE_PIPELINE_INIT_FN
title: PIBIO_STORAGE_PIPELINE_INIT_FN (winbio_adapter.h)
author: windows-sdk-content
description: Gives the Storage Adapter the chance to perform any initialization that remains incomplete.
old-location: secbiomet\storageadapterpipelineinit.htm
tech.root: SecBioMet
ms.assetid: F969AC5A-6760-4904-A04E-F2FEF4290F7A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_PIPELINE_INIT_FN, PIBIO_STORAGE_PIPELINE_INIT_FN callback, StorageAdapterPipelineInit, StorageAdapterPipelineInit callback function [Windows Biometric Framework API], secbiomet.storageadapterpipelineinit, winbio_adapter/StorageAdapterPipelineInit
ms.topic: callback
f1_keywords:
- winbio_adapter/StorageAdapterPipelineInit
dev_langs:
 - c++
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
- StorageAdapterPipelineInit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_STORAGE_PIPELINE_INIT_FN callback function


## -description


Called by the Windows Biometric Framework to give the Storage Adapter the chance to perform any initialization that remains incomplete.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


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



The Storage Adapter should return <b>S_OK</b> if it doesn’t need to perform any initialization at this point.

When this routine is called, the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn">SensorAdapterAttach</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn">EngineAdapterAttach</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn">StorageAdapterAttach</a> routines have completed normally.

This method executes in the context of an arbitrary RPC server thread.



