---
UID: NS:winbio_adapter._WINBIO_SENSOR_INTERFACE
title: WINBIO_SENSOR_INTERFACE (winbio_adapter.h)
author: windows-sdk-content
description: Contains pointers to your custom sensor adapter functions.
old-location: secbiomet\winbio_sensor_interface.htm
tech.root: SecBioMet
ms.assetid: ab5a7146-936f-4ee5-9864-4f5a3b774724
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWINBIO_SENSOR_INTERFACE, PWINBIO_SENSOR_INTERFACE, PWINBIO_SENSOR_INTERFACE structure pointer [Windows Biometric Framework API], WINBIO_SENSOR_INTERFACE, WINBIO_SENSOR_INTERFACE structure [Windows Biometric Framework API], secbiomet.winbio_sensor_interface, winbio_adapter/PWINBIO_SENSOR_INTERFACE, winbio_adapter/WINBIO_SENSOR_INTERFACE"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WINBIO_SENSOR_INTERFACE
product: Windows
targetos: Windows
req.typenames: "*PWINBIO_SENSOR_INTERFACE, WINBIO_SENSOR_INTERFACE"
req.redist: 
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

A pointer to your implementation of the <a href="https://msdn.microsoft.com/91243128-0543-4df9-bde8-74ef5ae46914">SensorAdapterAttach</a> function.


### -field Detach

A pointer to your implementation of the <a href="https://msdn.microsoft.com/58124c44-4343-44c1-84a2-c03455d68199">SensorAdapterDetach</a> function.


### -field ClearContext

A pointer to your implementation of the <a href="https://msdn.microsoft.com/a0743004-aa79-41d8-87c7-2a1b6f00a1f2">SensorAdapterClearContext</a> function.


### -field QueryStatus

A pointer to your implementation of the <a href="https://msdn.microsoft.com/88c22183-5bc8-4ac9-9048-72ee7a861b76">SensorAdapterQueryStatus</a> function.


### -field Reset

A pointer to your implementation of the <a href="https://msdn.microsoft.com/09a93726-2dff-4a8a-b36c-ad481a4f61b6">SensorAdapterReset</a> function.


### -field SetMode

A pointer to your implementation of the <a href="https://msdn.microsoft.com/83c4ecfa-da4f-41d3-b0ca-d654735743cd">SensorAdapterSetMode</a> function.


### -field SetIndicatorStatus

A pointer to your implementation of the <a href="https://msdn.microsoft.com/a47815d0-934c-43d4-8f4a-5f57a1c9f278">SensorAdapterSetIndicatorStatus</a> function.


### -field GetIndicatorStatus

A pointer to your implementation of the <a href="https://msdn.microsoft.com/01dbf2ee-5b47-47a8-b22c-a80aec5f7fff">SensorAdapterGetIndicatorStatus</a> function.


### -field StartCapture

A pointer to your implementation of the   <a href="https://msdn.microsoft.com/79922878-f5d3-4400-8c4f-2636323d7dcf">SensorAdapterStartCapture</a> function.


### -field FinishCapture

A pointer to your implementation of the   <a href="https://msdn.microsoft.com/f9ede590-5208-40ed-ac62-604a2d13a5a6">SensorAdapterFinishCapture</a> function.


### -field ExportSensorData

A pointer to your implementation of the   <a href="https://msdn.microsoft.com/a6e45371-169b-42a8-9a53-dd7b2928a754">SensorAdapterExportSensorData</a> function.


### -field Cancel

A pointer to your implementation of the   <a href="https://msdn.microsoft.com/11a0728e-1833-43b3-8ae2-0393743bb19b">SensorAdapterCancel</a> function.


### -field PushDataToEngine

A pointer to your implementation of the   <a href="https://msdn.microsoft.com/dea49f4b-668d-4b30-a16f-b74f260785c2">SensorAdapterPushDataToEngine</a> function.


### -field ControlUnit

A pointer to your implementation of the <a href="https://msdn.microsoft.com/cc37b9a0-bea8-4413-a2fe-30a92db74604">SensorAdapterControlUnit</a> function.


### -field ControlUnitPrivileged

A pointer to your implementation of the <a href="https://msdn.microsoft.com/373233e6-b3d0-40ce-8698-77841963d5f3">SensorAdapterControlUnitPrivileged</a>   function.


### -field NotifyPowerChange

A pointer to your implementation of the <a href="https://msdn.microsoft.com/7EA9D7E7-3DB9-4131-A747-B0388310ACB5">SensorAdapterNotifyPowerChange</a> function.  This member is supported starting in Windows 8.


### -field PipelineInit

A pointer to your implementation of the <a href="https://msdn.microsoft.com/91667505-78D6-405E-9028-DF4F3037B455">SensorAdapterPipelineInit</a> function. This member is supported starting in Windows 10.


### -field PipelineCleanup

A pointer to your implementation of the <a href="https://msdn.microsoft.com/36238A6F-BDE2-454E-A183-ED10A455AF13">SensorAdapterPipelineCleanup</a> function. This member is supported starting in Windows 10.


### -field Activate

A pointer to your implementation of the <a href="https://msdn.microsoft.com/CC5128D8-9863-4B9F-B82D-AE2A0D5A45C5">SensorAdapterActivate</a> function. This member is supported starting in Windows 10.


### -field Deactivate

A pointer to your implementation of the <a href="https://msdn.microsoft.com/2F10401B-5C0B-4376-AB4D-696FD1BEA079">SensorAdapterDeactivate</a> function. This member is supported starting in Windows 10.


### -field QueryExtendedInfo

A pointer to your implementation of the <a href="https://msdn.microsoft.com/28CC3757-5A9D-4E29-A26C-6FD90A38B45B">SensorAdapterQueryExtendedInfo</a> function. This member is supported starting in Windows 10.


### -field QueryCalibrationFormats

A pointer to your implementation of the <a href="https://msdn.microsoft.com/F8C97013-3BDA-445F-A2C2-60D08DD9C71A">SensorAdapterQueryCalibrationFormats</a> function. This member is supported starting in Windows 10.


### -field SetCalibrationFormat

A pointer to your implementation of the <a href="https://msdn.microsoft.com/06BC3CBF-AB51-47C8-BCFB-ADC3D920F27B">SensorAdapterSetCalibrationFormat</a> function. This member is supported starting in Windows 10.


### -field AcceptCalibrationData

A pointer to your implementation of the <a href="https://msdn.microsoft.com/EE3B7066-BE91-4F63-8E0A-70F5CAB46496">SensorAdapterAcceptCalibrationData</a> function. This member is supported starting in Windows 10.


### -field AsyncImportRawBuffer

 


### -field AsyncImportSecureBuffer

 


### -field QueryPrivateSensorType

 


### -field ConnectSecure

 


### -field StartCaptureEx

 


### -field StartNotifyWake

 


### -field FinishNotifyWake

 




## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/64fb908c-72c2-4639-a2f6-77ede080512c">Plug-in Structures</a>



<a href="https://msdn.microsoft.com/83ca38e1-3258-4676-bcdd-4876ec8f3ae1">WbioQuerySensorInterface</a>
 

 

