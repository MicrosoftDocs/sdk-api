---
UID: NS:winbio_adapter._WINBIO_ENGINE_INTERFACE
title: WINBIO_ENGINE_INTERFACE (winbio_adapter.h)
description: Contains pointers to your custom engine adapter functions.
helpviewer_keywords: ["*PWINBIO_ENGINE_INTERFACE","PWINBIO_ENGINE_INTERFACE","PWINBIO_ENGINE_INTERFACE structure pointer [Windows Biometric Framework API]","WINBIO_ENGINE_INTERFACE","WINBIO_ENGINE_INTERFACE structure [Windows Biometric Framework API]","secbiomet.winbio_engine_interface","winbio_adapter/PWINBIO_ENGINE_INTERFACE","winbio_adapter/WINBIO_ENGINE_INTERFACE"]
old-location: secbiomet\winbio_engine_interface.htm
tech.root: SecBioMet
ms.assetid: 04429f64-ae41-4c26-a777-bdb7aa92b685
ms.date: 12/05/2018
ms.keywords: '*PWINBIO_ENGINE_INTERFACE, PWINBIO_ENGINE_INTERFACE, PWINBIO_ENGINE_INTERFACE structure pointer [Windows Biometric Framework API], WINBIO_ENGINE_INTERFACE, WINBIO_ENGINE_INTERFACE structure [Windows Biometric Framework API], secbiomet.winbio_engine_interface, winbio_adapter/PWINBIO_ENGINE_INTERFACE, winbio_adapter/WINBIO_ENGINE_INTERFACE'
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
req.typenames: '*PWINBIO_ENGINE_INTERFACE, WINBIO_ENGINE_INTERFACE'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINBIO_ENGINE_INTERFACE
 - winbio_adapter/_WINBIO_ENGINE_INTERFACE
 - PWINBIO_ENGINE_INTERFACE
 - winbio_adapter/PWINBIO_ENGINE_INTERFACE
 - WINBIO_ENGINE_INTERFACE
 - winbio_adapter/WINBIO_ENGINE_INTERFACE
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
 - WINBIO_ENGINE_INTERFACE
---

# WINBIO_ENGINE_INTERFACE structure


## -description

The <b>WINBIO_ENGINE_INTERFACE</b> structure contains pointers to your custom engine adapter functions. The Windows Biometric Framework uses this structure to locate the functions.

## -struct-fields

### -field Version

Version number of this structure.

<b>Windows 10:  </b>The version number must be <b>WINBIO_ENGINE_INTERFACE_VERSION_3</b> or <b>WINBIO_ENGINE_INTERFACE_VERSION_4</b>. For more information on implementing <b>WINBIO_ENGINE_INTERFACE_VERSION_4</b>, see <a href="/windows/desktop/SecBioMet/sensor-requirements-for-secure-biometrics">Sensor requirements for secure biometrics</a>.

<b>Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:  </b>The version number must be <b>WINBIO_ENGINE_INTERFACE_VERSION_2</b>.

<b>Windows Server 2008 R2 and Windows 7:  </b>The version number must be <b>WINBIO_ENGINE_INTERFACE_VERSION_1</b>.

### -field Type

The type of adapter. This must be <b>WINBIO_ADAPTER_TYPE_ENGINE</b>.

### -field Size

The size, in bytes, of this structure. Set this value to the size of the <b>WINBIO_ENGINE_INTERFACE</b> structure.

### -field AdapterId

A GUID that uniquely identifies the engine adapter. You must generate this value.

### -field Attach

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn">EngineAdapterAttach</a> function.

### -field Detach

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn">EngineAdapterDetach</a> function.

### -field ClearContext

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn">EngineAdapterClearContext</a> function.

### -field QueryPreferredFormat

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn">EngineAdapterQueryPreferredFormat</a> function.

### -field QueryIndexVectorSize

A pointer to your implementation of the   <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn">EngineAdapterQueryIndexVectorSize</a> function.

### -field QueryHashAlgorithms

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn">EngineAdapterQueryHashAlgorithms</a> function.

### -field SetHashAlgorithm

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn">EngineAdapterSetHashAlgorithm</a> function.

### -field QuerySampleHint

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn">EngineAdapterQuerySampleHint</a> function.

### -field AcceptSampleData

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn">EngineAdapterAcceptSampleData</a> function.

### -field ExportEngineData

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn">EngineAdapterExportEngineData</a> function.

### -field VerifyFeatureSet

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn">EngineAdapterVerifyFeatureSet</a> function.

### -field IdentifyFeatureSet

A pointer to your implementation of the   <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn">EngineAdapterIdentifyFeatureSet</a> function.

### -field CreateEnrollment

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn">EngineAdapterCreateEnrollment</a> function.

### -field UpdateEnrollment

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn">EngineAdapterUpdateEnrollment</a> function.

### -field GetEnrollmentStatus

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn">EngineAdapterGetEnrollmentStatus</a> function.

### -field GetEnrollmentHash

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn">EngineAdapterGetEnrollmentHash</a> function.

### -field CheckForDuplicate

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn">EngineAdapterCheckForDuplicate</a> function.

### -field CommitEnrollment

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn">EngineAdapterCommitEnrollment</a> function.

### -field DiscardEnrollment

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn">EngineAdapterDiscardEnrollment</a> function.

### -field ControlUnit

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn">EngineAdapterControlUnit</a> function.

### -field ControlUnitPrivileged

A pointer to your implementation of the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn">EngineAdapterControlUnitPrivileged</a> function.

### -field NotifyPowerChange

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn">EngineAdapterNotifyPowerChange</a> function. This member is supported starting in Windows 8.

### -field Reserved_1

This field is reserved and should be set to <b>NULL</b>.

### -field PipelineInit

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn">EngineAdapterPipelineInit</a> function. This member is supported starting in Windows 10.

### -field PipelineCleanup

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn">EngineAdapterPipelineCleanup</a> function. This member is supported starting in Windows 10.

### -field Activate

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn">EngineAdapterActivate</a> function. This member is supported starting in Windows 10.

### -field Deactivate

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn">EngineAdapterDeactivate</a> function.  This member is supported starting in Windows 10.

### -field QueryExtendedInfo

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn">EngineAdapterQueryExtendedInfo</a> function. This member is supported starting in Windows 10.

### -field IdentifyAll

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn">EngineAdapterIdentifyAll</a> function. This member is supported starting in Windows 10.

### -field SetEnrollmentSelector

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn">EngineAdapterSetEnrollmentSelector</a> function. This member is supported starting in Windows 10.

### -field SetEnrollmentParameters

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn">EngineAdapterSetEnrollmentParameters</a> function. This member is supported starting in Windows 10.

### -field QueryExtendedEnrollmentStatus

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn">EngineAdapterQueryExtendedEnrollmentStatus</a> function. This member is supported starting in Windows 10.

### -field RefreshCache

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn">EngineAdapterRefreshCache</a> function. This member is supported starting in Windows 10.

### -field SelectCalibrationFormat

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn">EngineAdapterSelectCalibrationFormat</a> function. This member is supported starting in Windows 10.

### -field QueryCalibrationData

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn">EngineAdapterQueryCalibrationData</a> function. This member is supported starting in Windows 10.

### -field SetAccountPolicy

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn">EngineAdapterSetAccountPolicy</a> function. This member is supported starting in Windows 10.

### -field CreateKey

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn">EngineAdapterCreateKey</a> function. This member is supported starting in Windows 10, version 1607.

### -field IdentifyFeatureSetSecure

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn">EngineAdapterIdentifyFeatureSetSecure</a> function. This member is supported starting in Windows 10, version 1607.

### -field AcceptPrivateSensorTypeInfo

### -field CreateEnrollmentAuthenticated

### -field IdentifyFeatureSetAuthenticated

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/SecBioMet/plug-in-structures">Plug-in Structures</a>



<a href="/windows/desktop/api/winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface">WbioQueryEngineInterface</a>