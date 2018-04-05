---
UID: NS:winbio_types._WINBIO_EXTENDED_ENROLLMENT_STATUS
title: "_WINBIO_EXTENDED_ENROLLMENT_STATUS"
author: windows-driver-content
description: Contains additional information about the status of an enrollment that is in progress.
old-location: secbiomet\winbio_extended_enrollment_status.htm
old-project: SecBioMet
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_EXTENDED_ENROLLMENT_STATUS, PWINBIO_EXTENDED_ENROLLMENT_STATUS, PWINBIO_EXTENDED_ENROLLMENT_STATUS structure pointer [Windows Biometric Framework API], S_OK, WINBIO_EXTENDED_ENROLLMENT_STATUS, WINBIO_EXTENDED_ENROLLMENT_STATUS structure [Windows Biometric Framework API], WINBIO_E_BAD_CAPTURE, WINBIO_E_INVALID_OPERATION, WINBIO_I_MORE_DATA, _WINBIO_EXTENDED_ENROLLMENT_STATUS, secbiomet.winbio_extended_enrollment_status, winbio_types/PWINBIO_EXTENDED_ENROLLMENT_STATUS, winbio_types/WINBIO_EXTENDED_ENROLLMENT_STATUS"
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
req.typenames: WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS, WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winbio_types.h
api_name:
-	WINBIO_EXTENDED_ENROLLMENT_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_EXTENDED_ENROLLMENT_STATUS structure


## -description


Contains additional information about the status of an enrollment that is in progress.


## -struct-fields




### -field Specific

 Information about the status of an enrollment that is in progress for a specific biometric factor.



#### Null

Reserved. Must be zero.


### -field Specific.FacialFeatures

 Information about the status of an enrollment that is in progress for facial features.


### -field Specific.FacialFeatures.OpaqueEngineData

 


### -field Specific.FacialFeatures.BoundingBox

The position within the camera frame of the face of the  individual to enroll, in pixels. The size of the camera frame determines the upper limit on the number of pixels for this position. Get the  <b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO</b> property to determine the size of the camera frame.  A client that uses the presence monitor must perform the scaling operation to map the position  to the camera frame.


### -field Specific.FacialFeatures.Distance

The distance between the actual location of the face and the ideal focal distance for the face. This value ranges from -100 to 100. 0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.


### -field Specific.FacialFeatures.case

 


### -field Specific.Fingerprint

 Information about the status of an enrollment that is in progress for fingerprint patterns.


### -field Specific.Fingerprint.GeneralSamples

The total number of samples required to create a new fingerprint template.


### -field Specific.Fingerprint.Center

The number of samples for the center of the fingerprint required to create a new fingerprint template.


### -field Specific.Fingerprint.TopEdge

The number of samples for the top edge of the fingerprint required to create a new fingerprint template.


### -field Specific.Fingerprint.BottomEdge

The number of samples for the bottom edge of the fingerprint required to create a new fingerprint template.


### -field Specific.Fingerprint.LeftEdge

The number of samples for the left edge of the fingerprint required to create a new fingerprint template.


### -field Specific.Fingerprint.RightEdge

The number of samples for the right edge of the fingerprint required to create a new fingerprint template.


### -field Specific.Fingerprint.case

 


### -field Specific.Iris

 Information about the status of an enrollment that is in progress for iris patterns.


### -field Specific.Iris.EyeBoundingBox_1

The position within the camera frame of one of the  irises of the  individual to enroll, in pixels. If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye. If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame. If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual. 

The size of the camera frame determines the upper limit on the number of pixels for this position. Get the  <b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO</b> property to determine the size of the camera frame.  A client that uses the presence monitor must perform the scaling operation to map the position  to the camera frame.


### -field Specific.Iris.EyeBoundingBox_2

The position within the camera frame of one of the irises of the  individual to enroll, in pixels. If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty. If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.

The size of the camera frame determines the upper limit on the number of pixels for this position. Get the  <b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO</b> property to determine the size of the camera frame.  A client that uses the presence monitor must perform the scaling operation to map the position  to the camera frame.


### -field Specific.Iris.PupilCenter_1

The position of the center of one of the  pupils of the individual to enroll. If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye. If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame. If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual. 


### -field Specific.Iris.PupilCenter_2

The position of the center of one of the pupils of the individual to enroll.  If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty. If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.


### -field Specific.Iris.Distance

The distance between the actual location of the iris and the ideal focal distance for the iris. This value ranges from -100 to 100. 0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.


### -field Specific.Iris.case

 


### -field Specific.Voice

 Information about the status of an enrollment that is in progress for voice patterns.


### -field Specific.Voice.Reserved

Reserved.


### -field Specific.Voice.case

 


### -field TemplateStatus

The status of sample collection for the enrollment template. The following values are possible for this member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="S_OK"></a><a id="s_ok"></a><dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The enrollment is ready to be saved.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_E_INVALID_OPERATION"></a><a id="winbio_e_invalid_operation"></a><dl>
<dt><b>WINBIO_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
No enrollment is in progress.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_I_MORE_DATA"></a><a id="winbio_i_more_data"></a><dl>
<dt><b>WINBIO_I_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More samples are required to complete the template.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_E_BAD_CAPTURE"></a><a id="winbio_e_bad_capture"></a><dl>
<dt><b>WINBIO_E_BAD_CAPTURE</b></dt>
</dl>
</td>
<td width="60%">
The most recent sample is not usable.

</td>
</tr>
</table>
 


### -field RejectDetail

The reason that the most recent sample is unusable, if the value of the <b>TemplateStatus</b> member is <b>WINBIO_E_BAD_CAPTURE</b>.


### -field PercentComplete

The best estimate from the engine adapter for the percentage of the template that is complete, as a value from 0 to 100.


### -field Factor

The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter. For example, if the value of the <b>Factor</b> member is <b>WINBIO_TYPE_FINGERPRINT</b>, the <a href="https://msdn.microsoft.com/83586E04-24CA-4A39-836F-C80DB1508C71">WINBIO_EXTENDED_ENGINE_INFO</a> structure applies to a fingerprint reader and contains the relevant information in the <b>Specifc.Fingerprint</b> structure.


### -field SubFactor

A <b>WINBIO_BIOMETRIC_SUBTYPE</b> value that provides additional information about the enrollment. 

