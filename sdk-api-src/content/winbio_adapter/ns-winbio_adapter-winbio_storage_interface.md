---
UID: NS:winbio_adapter._WINBIO_STORAGE_INTERFACE
title: WINBIO_STORAGE_INTERFACE (winbio_adapter.h)
description: Contains pointers to your custom storage adapter functions.
helpviewer_keywords: ["*PWINBIO_STORAGE_INTERFACE","PWINBIO_STORAGE_INTERFACE","PWINBIO_STORAGE_INTERFACE structure pointer [Windows Biometric Framework API]","WINBIO_STORAGE_INTERFACE","WINBIO_STORAGE_INTERFACE structure [Windows Biometric Framework API]","secbiomet.winbio_storage_interface","winbio_adapter/PWINBIO_STORAGE_INTERFACE","winbio_adapter/WINBIO_STORAGE_INTERFACE"]
old-location: secbiomet\winbio_storage_interface.htm
tech.root: SecBioMet
ms.assetid: 1cc7ce07-66df-43d9-9db2-50558a0f5f47
ms.date: 12/05/2018
ms.keywords: '*PWINBIO_STORAGE_INTERFACE, PWINBIO_STORAGE_INTERFACE, PWINBIO_STORAGE_INTERFACE structure pointer [Windows Biometric Framework API], WINBIO_STORAGE_INTERFACE, WINBIO_STORAGE_INTERFACE structure [Windows Biometric Framework API], secbiomet.winbio_storage_interface, winbio_adapter/PWINBIO_STORAGE_INTERFACE, winbio_adapter/WINBIO_STORAGE_INTERFACE'
req.header: winbio_adapter.h
req.include-header: 
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
req.typenames: '*PWINBIO_STORAGE_INTERFACE, WINBIO_STORAGE_INTERFACE'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINBIO_STORAGE_INTERFACE
 - winbio_adapter/_WINBIO_STORAGE_INTERFACE
 - PWINBIO_STORAGE_INTERFACE
 - winbio_adapter/PWINBIO_STORAGE_INTERFACE
 - WINBIO_STORAGE_INTERFACE
 - winbio_adapter/WINBIO_STORAGE_INTERFACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WINBIO_STORAGE_INTERFACE
---

# WINBIO_STORAGE_INTERFACE structure


## -description

The <b>WINBIO_STORAGE_INTERFACE</b> structure contains pointers to your custom storage adapter functions. The Windows Biometric Framework uses this structure to locate the functions.

## -struct-fields

### -field Version

Version number of this structure.

<b>Windows 10:  </b>The version number must be <b>WINBIO_STORAGE_INTERFACE_VERSION_3</b>.

<b>Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:  </b>The version number must be <b>WINBIO_STORAGE_INTERFACE_VERSION_2</b>.

<b>Windows Server 2008 R2 and Windows 7:  </b>The version number must be <b>WINBIO_STORAGE_INTERFACE_VERSION_1</b>.

### -field Type

The type of adapter. This must be <b>WINBIO_ADAPTER_TYPE_STORAGE</b>.

### -field Size

The size, in bytes, of this structure. Set this value to the size of the <b>WINBIO_STORAGE_INTERFACE</b> structure.

### -field AdapterId

A GUID that uniquely identifies the storage adapter. You must generate this value.

### -field Attach

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn">StorageAdapterAttach</a> function.

### -field Detach

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn">StorageAdapterDetach</a> function.

### -field ClearContext

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn">StorageAdapterClearContext</a> function.

### -field CreateDatabase

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn">StorageAdapterCreateDatabase</a> function.

### -field EraseDatabase

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn">StorageAdapterEraseDatabase</a> function.

### -field OpenDatabase

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn">StorageAdapterOpenDatabase</a> function.

### -field CloseDatabase

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn">StorageAdapterCloseDatabase</a> function.

### -field GetDataFormat

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn">StorageAdapterGetDataFormat</a> function.

### -field GetDatabaseSize

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn">StorageAdapterGetDatabaseSize</a> function.

### -field AddRecord

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn">StorageAdapterAddRecord</a> function.

### -field DeleteRecord

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn">StorageAdapterDeleteRecord</a> function.

### -field QueryBySubject

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn">StorageAdapterQueryBySubject</a> function.

### -field QueryByContent

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn">StorageAdapterQueryByContent</a> function.

### -field GetRecordCount

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn">StorageAdapterGetRecordCount</a> function.

### -field FirstRecord

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn">StorageAdapterFirstRecord</a> function.

### -field NextRecord

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn">StorageAdapterNextRecord</a> function.

### -field GetCurrentRecord

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn">StorageAdapterGetCurrentRecord</a> function.

### -field ControlUnit

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn">StorageAdapterControlUnit</a> function.

### -field ControlUnitPrivileged

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn">StorageAdapterControlUnitPrivileged</a> function.

### -field NotifyPowerChange

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn">StorageAdapterNotifyPowerChange</a> function. This member is supported starting in Windows 8.

### -field PipelineInit

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn">StorageAdapterPipelineInit</a> function. This member is supported starting in Windows 10.

### -field PipelineCleanup

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn">StorageAdapterPipelineCleanup</a> function. This member is supported starting in Windows 10.

### -field Activate

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn">StorageAdapterActivate</a> function. This member is supported starting in Windows 10.

### -field Deactivate

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn">StorageAdapterDeactivate</a> function. This member is supported starting in Windows 10.

### -field QueryExtendedInfo

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn">StorageAdapterQueryExtendedInfo</a> function. This member is supported starting in Windows 10.

### -field NotifyDatabaseChange

### -field Reserved1

### -field Reserved2

### -field UpdateRecordBegin

### -field UpdateRecordCommit

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/SecBioMet/plug-in-structures">Plug-in Structures</a>



<a href="/windows/desktop/api/winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface">WbioQueryStorageInterface</a>