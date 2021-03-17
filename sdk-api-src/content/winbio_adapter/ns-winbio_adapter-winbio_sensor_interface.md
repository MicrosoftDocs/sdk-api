---
UID: NS:winbio_adapter._WINBIO_SENSOR_INTERFACE
title: WINBIO_SENSOR_INTERFACE (winbio_adapter.h)
description: Contains pointers to your custom sensor adapter functions.
helpviewer_keywords: ["*PWINBIO_SENSOR_INTERFACE","PWINBIO_SENSOR_INTERFACE","PWINBIO_SENSOR_INTERFACE structure pointer [Windows Biometric Framework API]","WINBIO_SENSOR_INTERFACE","WINBIO_SENSOR_INTERFACE structure [Windows Biometric Framework API]","secbiomet.winbio_sensor_interface","winbio_adapter/PWINBIO_SENSOR_INTERFACE","winbio_adapter/WINBIO_SENSOR_INTERFACE"]
old-location: secbiomet\winbio_sensor_interface.htm
tech.root: SecBioMet
ms.assetid: ab5a7146-936f-4ee5-9864-4f5a3b774724
ms.date: 12/05/2018
ms.keywords: '*PWINBIO_SENSOR_INTERFACE, PWINBIO_SENSOR_INTERFACE, PWINBIO_SENSOR_INTERFACE structure pointer [Windows Biometric Framework API], WINBIO_SENSOR_INTERFACE, WINBIO_SENSOR_INTERFACE structure [Windows Biometric Framework API], secbiomet.winbio_sensor_interface, winbio_adapter/PWINBIO_SENSOR_INTERFACE, winbio_adapter/WINBIO_SENSOR_INTERFACE'
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
req.typenames: '*PWINBIO_SENSOR_INTERFACE, WINBIO_SENSOR_INTERFACE'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINBIO_SENSOR_INTERFACE
 - winbio_adapter/_WINBIO_SENSOR_INTERFACE
 - PWINBIO_SENSOR_INTERFACE
 - winbio_adapter/PWINBIO_SENSOR_INTERFACE
 - WINBIO_SENSOR_INTERFACE
 - winbio_adapter/WINBIO_SENSOR_INTERFACE
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
 - WINBIO_SENSOR_INTERFACE
---

# WINBIO_SENSOR_INTERFACE structure


## -description

The <b>WINBIO_SENSOR_INTERFACE</b> structure contains pointers to your custom sensor adapter functions. The Windows Biometric Framework uses this structure to locate the functions.

## -struct-fields

### -field Version

Version number of this structure.

<b>Windows 10:  </b>The version number must be <b>WINBIO_SENSOR_INTERFACE_VERSION_3</b>.

<b>Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:  </b>The version number must be <b>WINBIO_SENSOR_INTERFACE_VERSION_2</b>.

<b>Windows Server 2008 R2 and Windows 7:  </b>The version number must be <b>WINBIO_SENSOR_INTERFACE_VERSION_1</b>.

### -field Type

The type of adapter. This must be <b>WINBIO_ADAPTER_TYPE_SENSOR</b>.

### -field Size

The size, in bytes, of this structure. Set this value to the size of the <b>WINBIO_SENSOR_INTERFACE</b> structure.

### -field AdapterId

A GUID that uniquely identifies the sensor adapter. You must generate this value.

### -field Attach

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn">SensorAdapterAttach</a> function.

### -field Detach

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn">SensorAdapterDetach</a> function.

### -field ClearContext

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn">SensorAdapterClearContext</a> function.

### -field QueryStatus

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn">SensorAdapterQueryStatus</a> function.

### -field Reset

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn">SensorAdapterReset</a> function.

### -field SetMode

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn">SensorAdapterSetMode</a> function.

### -field SetIndicatorStatus

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn">SensorAdapterSetIndicatorStatus</a> function.

### -field GetIndicatorStatus

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn">SensorAdapterGetIndicatorStatus</a> function.

### -field StartCapture

A pointer to your implementation of the   <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn">SensorAdapterStartCapture</a> function.

### -field FinishCapture

A pointer to your implementation of the   <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn">SensorAdapterFinishCapture</a> function.

### -field ExportSensorData

A pointer to your implementation of the   <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn">SensorAdapterExportSensorData</a> function.

### -field Cancel

A pointer to your implementation of the   <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn">SensorAdapterCancel</a> function.

### -field PushDataToEngine

A pointer to your implementation of the   <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn">SensorAdapterPushDataToEngine</a> function.

### -field ControlUnit

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn">SensorAdapterControlUnit</a> function.

### -field ControlUnitPrivileged

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn">SensorAdapterControlUnitPrivileged</a>   function.

### -field NotifyPowerChange

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn">SensorAdapterNotifyPowerChange</a> function.  This member is supported starting in Windows 8.

### -field PipelineInit

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn">SensorAdapterPipelineInit</a> function. This member is supported starting in Windows 10.

### -field PipelineCleanup

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn">SensorAdapterPipelineCleanup</a> function. This member is supported starting in Windows 10.

### -field Activate

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn">SensorAdapterActivate</a> function. This member is supported starting in Windows 10.

### -field Deactivate

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn">SensorAdapterDeactivate</a> function. This member is supported starting in Windows 10.

### -field QueryExtendedInfo

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn">SensorAdapterQueryExtendedInfo</a> function. This member is supported starting in Windows 10.

### -field QueryCalibrationFormats

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn">SensorAdapterQueryCalibrationFormats</a> function. This member is supported starting in Windows 10.

### -field SetCalibrationFormat

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn">SensorAdapterSetCalibrationFormat</a> function. This member is supported starting in Windows 10.

### -field AcceptCalibrationData

A pointer to your implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn">SensorAdapterAcceptCalibrationData</a> function. This member is supported starting in Windows 10.

### -field AsyncImportRawBuffer

### -field AsyncImportSecureBuffer

### -field QueryPrivateSensorType

### -field ConnectSecure

### -field StartCaptureEx

### -field StartNotifyWake

### -field FinishNotifyWake

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/SecBioMet/plug-in-structures">Plug-in Structures</a>



<a href="/windows/desktop/api/winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface">WbioQuerySensorInterface</a>