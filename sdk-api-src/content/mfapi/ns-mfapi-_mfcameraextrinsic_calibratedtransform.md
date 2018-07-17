---
UID: NS:mfapi._MFCameraExtrinsic_CalibratedTransform
title: "_MFCameraExtrinsic_CalibratedTransform"
author: windows-sdk-content
description: A transform describing the location of a camera relative to other cameras or an established external reference.
old-location: mf\mfcameraextrinsic_calibratedtransform.htm
old-project: medfound
ms.assetid: 2D227167-68DC-4A43-8665-9A253BD66401
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: MFCameraExtrinsic_CalibratedTransform, MFCameraExtrinsic_CalibratedTransform structure [Media Foundation], PMFCameraExtrinsic_CalibratedTransform, PMFCameraExtrinsic_CalibratedTransform structure pointer [Media Foundation], _MFCameraExtrinsic_CalibratedTransform, mf.mfcameraextrinsic_calibratedtransform, mfapi/MFCameraExtrinsic_CalibratedTransform, mfapi/PMFCameraExtrinsic_CalibratedTransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfapi.h
req.include-header: 
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
tech.root: 
req.typenames: MFCameraExtrinsic_CalibratedTransform
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFCameraExtrinsic_CalibratedTransform
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFCameraExtrinsic_CalibratedTransform structure


## -description


A transform describing the location of a camera relative to other cameras or an established external reference.


## -struct-fields




### -field CalibrationId

A reference GUID identifying the calibration process for the data, allowing different consumers to identify calibration data from the same process.


### -field Position

The transform position.


### -field Orientation

The transform rotation.


## -remarks



The <b>Position</b> value should be expressed in real-world coordinates in units of meters. The coordinate system of both position and orientation should be right-handed Cartesian as shown in the following diagram. 

<img alt="Right-handed Cartesian coordinate system" src="./images/MFCameraExtrinsic_Diagram.png"/>
<div class="alert"><b>Important</b>  <p class="note">The position and orientation are expressed as transforms toward the reference frame or origin. For example, a <b>Position</b> value of {-5, 0, 0} means that the origin is 5 meters to the left of the sensor, and therefore the sensor is 5 meters to the right of the origin. A sensor that is positioned 2 meters above the origin should specify a <b>Position</b> of {0, -2, 0} because that is the translation from the sensor to the origin.

<p class="note">If the sensor is aligned with the origin, the rotation is the identity quaternion and the forward vector is along the -Z axis  {0, 0, -1}. If the sensor is rotated +30 degrees around the Y axis from the origin, then the <b>Orientation</b> value should be a rotation of -30 degrees around the Y axis, because it represents the rotation from the sensor to the origin.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

