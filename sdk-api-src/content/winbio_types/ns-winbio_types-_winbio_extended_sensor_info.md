---
UID: NS:winbio_types._WINBIO_EXTENDED_SENSOR_INFO
title: "_WINBIO_EXTENDED_SENSOR_INFO"
author: windows-driver-content
description: Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.
old-location: secbiomet\winbio_extended_sensor_info.htm
old-project: SecBioMet
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_EXTENDED_SENSOR_INFO, PWINBIO_EXTENDED_SENSOR_INFO, PWINBIO_EXTENDED_SENSOR_INFO structure pointer [Windows Biometric Framework API], WINBIO_EXTENDED_SENSOR_INFO, WINBIO_EXTENDED_SENSOR_INFO structure [Windows Biometric Framework API], _WINBIO_EXTENDED_SENSOR_INFO, secbiomet.winbio_extended_sensor_info, winbio_types/PWINBIO_EXTENDED_SENSOR_INFO, winbio_types/WINBIO_EXTENDED_SENSOR_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_types.h
req.include-header: Winbio.h for client applications or Winbio_adapters.h for adapters
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
req.typenames: WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO, WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winbio_types.h
api_name:
-	WINBIO_EXTENDED_SENSOR_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_EXTENDED_SENSOR_INFO structure


## -description


Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.


## -struct-fields




### -field Specific

Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to a specific biometric factor.



#### Null

Reserved. Must be zero.


### -field Specific.FacialFeatures

Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to facial features.


### -field Specific.FacialFeatures.HardwareInfo

 


### -field Specific.FacialFeatures.FrameSize

The size of the camera frame, indicated as a length and width in pixels by the <b>right</b> and <b>bottom</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure. The point (0, 0) represents the top-left corner of the frame.


### -field Specific.FacialFeatures.FrameOffset

The offset of the camera frame for the face from the video camera, in pixels. A value of (0, 0) indicates that the camera frame for the face and the video camera completely overlap.


### -field Specific.FacialFeatures.MandatoryOrientation

The preferred orientation for the camera.


### -field Specific.FacialFeatures.case

 


### -field Specific.Fingerprint

Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to fingerprint patterns.


### -field Specific.Fingerprint.Reserved

Reserved.


### -field Specific.Fingerprint.case

 


### -field Specific.Iris

Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to iris patterns.


### -field Specific.Iris.FrameSize

The size of the camera frame, indicated as a length and width in pixels by the <b>right</b> and <b>bottom</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure. The point (0, 0) represents the top-left corner of the frame.


### -field Specific.Iris.FrameOffset

The offset of the camera frame for the iris from the video camera, in pixels. A value of (0, 0) indicates that the camera frame for the iris and the video camera completely overlap.


### -field Specific.Iris.MandatoryOrientation

The preferred orientation for the camera.


### -field Specific.Iris.case

 


### -field Specific.Voice

Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to voice patterns.


### -field Specific.Voice.Reserved

Reserved.


### -field Specific.Voice.case

 


### -field GenericSensorCapabilities

The generic capabilities of the sensor component that is connected to a specific biometric unit. 


### -field Factor

The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the sensor adapter. For example, if the value of the <b>Factor</b> member is <b>WINBIO_TYPE_FINGERPRINT</b>, the <b>WINBIO_EXTENDED_SENSOR_INFO</b> structure applies to a fingerprint reader and contains the relevant information in the <b>Specifc.Fingerprint</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/DCBDB5F9-FF81-44C1-B439-2B8C02483212">WINBIO_BIOMETRIC_TYPE Constants</a>



<a href="https://msdn.microsoft.com/D447273E-2A02-484E-B0E4-69FEADD15797">WINBIO_CAPABILITY Constants</a>



<a href="https://msdn.microsoft.com/E44A6F17-5F38-47C7-947B-FB6FB79B1217">WINBIO_ORIENTATION Constants</a>
 

 

