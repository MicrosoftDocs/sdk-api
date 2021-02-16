---
UID: NC:winbio_adapter.PIBIO_STORAGE_GET_DATABASE_SIZE_FN
title: PIBIO_STORAGE_GET_DATABASE_SIZE_FN (winbio_adapter.h)
description: Retrieves the database size and available space.
helpviewer_keywords: ["PIBIO_STORAGE_GET_DATABASE_SIZE_FN","PIBIO_STORAGE_GET_DATABASE_SIZE_FN callback","StorageAdapterGetDatabaseSize","StorageAdapterGetDatabaseSize callback function [Windows Biometric Framework API]","secbiomet.storageadaptergetdatabasesize","winbio_adapter/StorageAdapterGetDatabaseSize"]
old-location: secbiomet\storageadaptergetdatabasesize.htm
tech.root: SecBioMet
ms.assetid: 98e26b32-3e2a-40d9-8463-9bd7e93c636b
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_GET_DATABASE_SIZE_FN, PIBIO_STORAGE_GET_DATABASE_SIZE_FN callback, StorageAdapterGetDatabaseSize, StorageAdapterGetDatabaseSize callback function [Windows Biometric Framework API], secbiomet.storageadaptergetdatabasesize, winbio_adapter/StorageAdapterGetDatabaseSize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_STORAGE_GET_DATABASE_SIZE_FN
 - winbio_adapter/PIBIO_STORAGE_GET_DATABASE_SIZE_FN
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
 - StorageAdapterGetDatabaseSize
---

# PIBIO_STORAGE_GET_DATABASE_SIZE_FN callback function


## -description

Called by the Windows Biometric Framework to retrieve the database size and available space.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param AvailableRecordCount [out]

Pointer to a variable that receives the number of unused record slots in the database.

### -param TotalRecordCount [out]

Pointer to a variable that receives the number of valid records in the database.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

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
A mandatory pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>StorageContext</b> member of the pipeline object is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>