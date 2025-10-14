---
UID: NC:winbio_adapter.PIBIO_STORAGE_OPEN_DATABASE_FN
title: PIBIO_STORAGE_OPEN_DATABASE_FN (winbio_adapter.h)
description: Opens a database for use by the storage adapter.
helpviewer_keywords: ["PIBIO_STORAGE_OPEN_DATABASE_FN","PIBIO_STORAGE_OPEN_DATABASE_FN callback","StorageAdapterOpenDatabase","StorageAdapterOpenDatabase callback function [Windows Biometric Framework API]","secbiomet.storageadapteropendatabase","winbio_adapter/StorageAdapterOpenDatabase"]
old-location: secbiomet\storageadapteropendatabase.htm
tech.root: SecBioMet
ms.assetid: 4f3dfa67-5020-461a-b3d1-33c948129bdf
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_OPEN_DATABASE_FN, PIBIO_STORAGE_OPEN_DATABASE_FN callback, StorageAdapterOpenDatabase, StorageAdapterOpenDatabase callback function [Windows Biometric Framework API], secbiomet.storageadapteropendatabase, winbio_adapter/StorageAdapterOpenDatabase
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
 - PIBIO_STORAGE_OPEN_DATABASE_FN
 - winbio_adapter/PIBIO_STORAGE_OPEN_DATABASE_FN
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
 - StorageAdapterOpenDatabase
---

# PIBIO_STORAGE_OPEN_DATABASE_FN callback function


## -description

Called by the Windows Biometric Framework to open a database.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param DatabaseId [in]

Pointer to a GUID that uniquely identifies the database. This is the same GUID used to register the database in the registry.

### -param FilePath [in]

Pointer to a <b>NULL</b>-terminated Unicode string that contains the fully qualified file path for the database.

### -param ConnectString [in]

Pointer to a <b>NULL</b>-terminated Unicode connection string for the database.

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
<dt><b>WINBIO_E_DATABASE_CANT_CREATE</b></dt>
</dl>
</td>
<td width="60%">
The database cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DATABASE_CANT_FIND</b></dt>
</dl>
</td>
<td width="60%">
The specified database cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DATABASE_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The database is currently locked by another application and cannot be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DATABASE_CANT_OPEN</b></dt>
</dl>
</td>
<td width="60%">
An unspecified problem has caused the request to fail.

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



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn">StorageAdapterCloseDatabase</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn">StorageAdapterCreateDatabase</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn">StorageAdapterEraseDatabase</a>