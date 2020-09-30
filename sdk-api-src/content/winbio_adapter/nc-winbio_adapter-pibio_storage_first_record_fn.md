---
UID: NC:winbio_adapter.PIBIO_STORAGE_FIRST_RECORD_FN
title: PIBIO_STORAGE_FIRST_RECORD_FN (winbio_adapter.h)
description: Positions the result set cursor on the first record in the set.
helpviewer_keywords: ["PIBIO_STORAGE_FIRST_RECORD_FN","PIBIO_STORAGE_FIRST_RECORD_FN callback","StorageAdapterFirstRecord","StorageAdapterFirstRecord callback function [Windows Biometric Framework API]","secbiomet.storageadapterfirstrecord","winbio_adapter/StorageAdapterFirstRecord"]
old-location: secbiomet\storageadapterfirstrecord.htm
tech.root: SecBioMet
ms.assetid: 736688c3-2c2c-4244-9f49-98ad0fe2d141
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_FIRST_RECORD_FN, PIBIO_STORAGE_FIRST_RECORD_FN callback, StorageAdapterFirstRecord, StorageAdapterFirstRecord callback function [Windows Biometric Framework API], secbiomet.storageadapterfirstrecord, winbio_adapter/StorageAdapterFirstRecord
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
 - PIBIO_STORAGE_FIRST_RECORD_FN
 - winbio_adapter/PIBIO_STORAGE_FIRST_RECORD_FN
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
 - StorageAdapterFirstRecord
---

# PIBIO_STORAGE_FIRST_RECORD_FN callback function


## -description

Called by the Windows Biometric Framework or by an engine adapter to position the result set cursor on the first record in the set.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

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
The <i>Pipeline</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DATABASE_NO_RESULTS</b></dt>
</dl>
</td>
<td width="60%">
There are no records in the result set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>StorageContext</b> member of the pipeline object is <b>NULL</b> or the <b>FileHandle</b> member is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn">StorageAdapterGetCurrentRecord</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn">StorageAdapterNextRecord</a>