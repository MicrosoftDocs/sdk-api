---
UID: NC:winbio_adapter.PIBIO_STORAGE_GET_DATA_FORMAT_FN
title: PIBIO_STORAGE_GET_DATA_FORMAT_FN (winbio_adapter.h)
description: Retrieves format and version information used by the current database associated with the pipeline.
helpviewer_keywords: ["PIBIO_STORAGE_GET_DATA_FORMAT_FN","PIBIO_STORAGE_GET_DATA_FORMAT_FN callback","StorageAdapterGetDataFormat","StorageAdapterGetDataFormat callback function [Windows Biometric Framework API]","secbiomet.storageadaptergetdataformat","winbio_adapter/StorageAdapterGetDataFormat"]
old-location: secbiomet\storageadaptergetdataformat.htm
tech.root: SecBioMet
ms.assetid: e5bf31aa-59d7-410a-bb11-fe4af36fa409
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_GET_DATA_FORMAT_FN, PIBIO_STORAGE_GET_DATA_FORMAT_FN callback, StorageAdapterGetDataFormat, StorageAdapterGetDataFormat callback function [Windows Biometric Framework API], secbiomet.storageadaptergetdataformat, winbio_adapter/StorageAdapterGetDataFormat
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
 - PIBIO_STORAGE_GET_DATA_FORMAT_FN
 - winbio_adapter/PIBIO_STORAGE_GET_DATA_FORMAT_FN
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
 - StorageAdapterGetDataFormat
---

# PIBIO_STORAGE_GET_DATA_FORMAT_FN callback function


## -description

Called by the Windows Biometric Framework to retrieve format and version information used by the current database associated with the pipeline.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param Format [out]

Pointer to a variable that receives a  GUID that uniquely identifies the data format used by this storage adapter when it stores templates in the database.

### -param Version [out]

Pointer to a <a href="/windows/desktop/SecBioMet/winbio-version">WINBIO_VERSION</a>  structure that receives the version number of the storage adapter component.

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