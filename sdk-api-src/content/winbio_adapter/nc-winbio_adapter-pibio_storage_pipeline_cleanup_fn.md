---
UID: NC:winbio_adapter.PIBIO_STORAGE_PIPELINE_CLEANUP_FN
title: PIBIO_STORAGE_PIPELINE_CLEANUP_FN (winbio_adapter.h)
description: Gives the Storage Adapter the chance to perform any cleanup in preparation for closing the template database.
helpviewer_keywords: ["PIBIO_STORAGE_PIPELINE_CLEANUP_FN","PIBIO_STORAGE_PIPELINE_CLEANUP_FN callback","StorageAdapterPipelineCleanup","StorageAdapterPipelineCleanup callback function [Windows Biometric Framework API]","secbiomet.storageadapterpipelinecleanup","winbio_adapter/StorageAdapterPipelineCleanup"]
old-location: secbiomet\storageadapterpipelinecleanup.htm
tech.root: SecBioMet
ms.assetid: 4F75BCE0-173F-48F3-B4DD-A6AE1AFD4EA5
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_PIPELINE_CLEANUP_FN, PIBIO_STORAGE_PIPELINE_CLEANUP_FN callback, StorageAdapterPipelineCleanup, StorageAdapterPipelineCleanup callback function [Windows Biometric Framework API], secbiomet.storageadapterpipelinecleanup, winbio_adapter/StorageAdapterPipelineCleanup
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
 - PIBIO_STORAGE_PIPELINE_CLEANUP_FN
 - winbio_adapter/PIBIO_STORAGE_PIPELINE_CLEANUP_FN
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
 - StorageAdapterPipelineCleanup
---

# PIBIO_STORAGE_PIPELINE_CLEANUP_FN callback function


## -description

Called by the Windows Biometric Framework to give the Storage Adapter the chance to perform any cleanup in preparation for closing the template database.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

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

The Storage Adapter should return <b>S_OK</b> if it doesn’t need to perform any cleanup at this point.

This method executes in the context of an arbitrary RPC server thread.