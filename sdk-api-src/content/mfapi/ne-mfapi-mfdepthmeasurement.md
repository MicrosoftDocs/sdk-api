---
UID: NE:mfapi._MFDepthMeasurement
title: MFDepthMeasurement
ms.date: 
targetos: Windows
description: Specifies the measurement system for a depth value in a video frame.
helpviewer_keywords: ["MFDepthMeasurement","mfapi/MFDepthMeasurement"]
tech.root: mf
req.construct-type: enumeration
req.ddi-compliance: 
req.header: mfapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - _MFDepthMeasurement
 - MFDepthMeasurement
f1_keywords:
 - _MFDepthMeasurement
 - mfapi/_MFDepthMeasurement
 - MFDepthMeasurement
 - mfapi/MFDepthMeasurement
dev_langs:
 - c++
---

## -description

Specifies the measurement system for a depth value in a video frame.

## -enum-fields

### -field DistanceToFocalPlane:0

The measurement is the distance to the focal plane.

### -field DistanceToOpticalCenter:1

The measurement is the distance to the optical center.

## -remarks

Use a value from this enumeration with the [MF_MT_DEPTH_MEASUREMENT](/windows/win32/medfound/mf-mt-depth-measurement) attribute.

The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.

![Illustration of DistanceToFocalPlane](images/distance_to_focal_plane.png)

The distance to focal center format is typically raw data from sensor such as time of flight cameras.

![Illustration of DistanceToOpticalCenter](images/distance_to_optical_center.png)
  

## -see-also

