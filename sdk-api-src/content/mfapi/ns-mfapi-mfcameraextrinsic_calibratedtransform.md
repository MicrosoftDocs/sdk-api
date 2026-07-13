---
UID: NS:mfapi._MFCameraExtrinsic_CalibratedTransform
title: MFCameraExtrinsic_CalibratedTransform (mfapi.h)
description: A transform describing the location of a camera relative to other cameras or an established external reference.
helpviewer_keywords: ["MFCameraExtrinsic_CalibratedTransform","MFCameraExtrinsic_CalibratedTransform structure [Media Foundation]","PMFCameraExtrinsic_CalibratedTransform","PMFCameraExtrinsic_CalibratedTransform structure pointer [Media Foundation]","mf.mfcameraextrinsic_calibratedtransform","mfapi/MFCameraExtrinsic_CalibratedTransform","mfapi/PMFCameraExtrinsic_CalibratedTransform"]
old-location: mf\mfcameraextrinsic_calibratedtransform.htm
tech.root: mf
ms.assetid: 2D227167-68DC-4A43-8665-9A253BD66401
ms.date: 12/05/2018
ms.keywords: MFCameraExtrinsic_CalibratedTransform, MFCameraExtrinsic_CalibratedTransform structure [Media Foundation], PMFCameraExtrinsic_CalibratedTransform, PMFCameraExtrinsic_CalibratedTransform structure pointer [Media Foundation], mf.mfcameraextrinsic_calibratedtransform, mfapi/MFCameraExtrinsic_CalibratedTransform, mfapi/PMFCameraExtrinsic_CalibratedTransform
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFCameraExtrinsic_CalibratedTransform
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFCameraExtrinsic_CalibratedTransform
 - mfapi/_MFCameraExtrinsic_CalibratedTransform
 - MFCameraExtrinsic_CalibratedTransform
 - mfapi/MFCameraExtrinsic_CalibratedTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFCameraExtrinsic_CalibratedTransform
---

# MFCameraExtrinsic_CalibratedTransform structure


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

<img alt="Right-handed Cartesian coordinate system" src="images/MFCameraExtrinsic_Diagram.png"/>
<div class="alert"><b>Important</b>
  <p class="note">The <b>Position</b> and <b>Orientation</b> have different interpretations for stand-alone sensor groups, and for Windows Mixed Reality devices.
</div>
  
### Stand-alone sensor groups
<p class="note">For stand-alone sensor groups, the position and orientation express the location of the origin of the group in the sensor's coordinate system. For example, a <b>Position</b> value of {-5, 0, 0} means that the origin is 5 meters to the left of the sensor, and therefore the sensor is 5 meters to the right of the origin. A sensor that is positioned 2 meters above the origin should specify a <b>Position</b> of {0, -2, 0} because that is the position of the origin relative to the sensor.

<p class="note">If the sensor is aligned with the origin, the rotation is the identity quaternion and the forward vector is along the -Z axis  {0, 0, -1}. If the sensor is rotated +30 degrees around the Y axis from the origin (i.e. to the left), then the <b>Orientation</b> value should be a rotation of -30 degrees around the Y axis, because it represents the orientation of the origin, relative to the sensor.

### Windows Mixed Reality devices
<p class="note">Sensors attached to a Windows Mixed Reality device (e.g. a HoloLens) express their calibration using the opposite convention, so the position and orientation indicate the location of the <em>sensor</em> in the <em>device's</em> coordinate system. For example, a sensor which is located 5 centimeters to the right of the origin of the device will have a <b>Position</b> of {0.05, 0, 0} because that is the position of the sensor, relative to the device. Likewise, if a sensor is rotated +10 degrees around the Y axis from the device (i.e. to the left), then the <b>Orientation</b> value will be a rotation of +10 degrees about the Y axis, because it represents the orientation of the sensor, relative to the device.
  
In addition, the <b>CalibrationId</b> can be passed to <a href="/uwp/api/windows.perception.spatial.preview.spatialgraphinteroppreview.createlocatorfornode">SpatialGraphInteropPreview.CreateLocatorForNode</a> to create a <a href="/uwp/api/windows.perception.spatial.spatiallocator">SpatialLocator</a> which represents the Windows Mixed Reality device. This can be used to compute the location of the sensor in space for a given frame, by querying the location of the <b>SpatialLocator</b> at the time the frame was captured, and combining this with the <b>Position</b> and <b>Orientation</b> of the <b>MFCameraExtrinsic_CalibratedTransform</b>. To query the device's location for a frame, pass the timestamp of the frame given by <a href="/windows/win32/api/mfobjects/nf-mfobjects-imfsample-getsampletime">IMFSample::GetSampleTime</a> to <a href="/uwp/api/windows.perception.perceptiontimestamphelper.fromsystemrelativetargettime">PerceptionTimestampHelper.FromSystemRelativeTargetTime</a>, and pass the resulting <b>PerceptionTimestamp</b> to <a href="/uwp/api/windows.perception.spatial.spatiallocator.trylocateattimestamp">SpatialLocator.TryLocateAtTimestamp</a>.

To determine whether an <b>IMFSample</b> came from a sensor attached to a Windows Mixed Reality device, look for the following property attached to the frame, set to `MFCameraExtrinsicsCalibrationType_SpatialGraphDynamicNode`:

```cpp
typedef enum _MFCameraExtrinsicsCalibrationType
{
    MFCameraExtrinsicsCalibrationType_Unknown = 0,
    MFCameraExtrinsicsCalibrationType_SpatialGraphDynamicNode = 1
} MFCameraExtrinsicsCalibrationType;

DEFINE_GUID(MFSampleExtension_CameraExtrinsicsCalibrationType, 0x3524e3b0, 0xc355, 0x49f1, 0xb8, 0xb0, 0xd0, 0xdd, 0x62, 0xde, 0x37, 0xa7);
```

<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
