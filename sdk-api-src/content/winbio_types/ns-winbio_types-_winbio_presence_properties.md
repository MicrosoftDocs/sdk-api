---
UID: NS:winbio_types._WINBIO_PRESENCE_PROPERTIES
title: "_WINBIO_PRESENCE_PROPERTIES"
author: windows-driver-content
description: Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.
old-location: secbiomet\winbio_presence_properties.htm
old-project: SecBioMet
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_PRESENCE_PROPERTIES, PWINBIO_PRESENCE_PROPERTIES, PWINBIO_PRESENCE_PROPERTIES union pointer [Windows Biometric Framework API], WINBIO_PRESENCE_PROPERTIES, WINBIO_PRESENCE_PROPERTIES union [Windows Biometric Framework API], _WINBIO_PRESENCE_PROPERTIES, secbiomet.winbio_presence_properties, winbio_types/PWINBIO_PRESENCE_PROPERTIES, winbio_types/WINBIO_PRESENCE_PROPERTIES"
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
req.typenames: WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES, WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winbio_types.h
api_name:
-	WINBIO_PRESENCE_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_PRESENCE_PROPERTIES structure


## -description


Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.


## -struct-fields




### -field FacialFeatures

Values for the location of facial features that the Windows Biometric Framework used to determine that an individual was present.



#### BoundingBox

The position within the camera frame of the face of the  individual, in pixels. The size of the camera frame determines the upper limit on the number of pixels for this position. Get the  <b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO</b> property to determine the size of the camera frame.  A client that uses the presence monitor must perform the scaling operation to map the position  to the camera frame .



#### Distance

The distance between the actual location of the face and the ideal focal distance for the face. This value ranges from -100 to 100. 0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.


### -field FacialFeatures.OpaqueEngineData

 


### -field FacialFeatures.OpaqueEngineData.AdapterId

 


### -field FacialFeatures.OpaqueEngineData.Data

 


### -field Iris

Values for iris location that the Windows Biometric Framework used to determine that an individual was present.



#### EyeBoundingBox_1

The position within the camera frame of one of the  irises of the  individual to enroll, in pixels. If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye. If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame. If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual. 

The size of the camera frame determines the upper limit on the number of pixels for this position. Get the  <b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO</b> property to determine the size of the camera frame.  A client that uses the presence monitor must perform the scaling operation to map the position  to the camera frame.



#### EyeBoundingBox_2

The position within the camera frame of one of the irises of the  individual to enroll, in pixels. If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty. If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.

The size of the camera frame determines the upper limit on the number of pixels for this position. Get the  <b>WINBIO_PROPERTY_EXTENDED_SENSOR_INFO</b> property to determine the size of the camera frame.  A client that uses the presence monitor must perform the scaling operation to map the position  to the camera frame.



#### PupilCenter_1

The position of the center of one of the  pupils of the individual to enroll. If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye. If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame. If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual. 



#### PupilCenter_2

The position of the center of one of the pupils of the individual to enroll.  If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty. If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.



#### Distance

The distance between the actual location of the iris and the ideal focal distance for the iris. This value ranges from -100 to 100. 0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.


### -field Null

 


### -field switch_type

 



