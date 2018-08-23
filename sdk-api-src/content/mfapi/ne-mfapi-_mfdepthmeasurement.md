---
UID: NE:mfapi._MFDepthMeasurement
title: "_MFDepthMeasurement"
author: windows-sdk-content
description: Specifies the measurement system for a depth value in a video frame.
old-location: mf\_mfdepthmeasurement.htm
old-project: medfound
ms.assetid: CCE34279-A52C-4F6E-9E8E-679F76187B3B
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DistanceToFocalPlane, DistanceToOpticalCenter, MFDepthMeasurement, _MFDepthMeasurement, _MFDepthMeasurement enumeration [Media Foundation], mf._mfdepthmeasurement, mfapi/DistanceToFocalPlane, mfapi/DistanceToOpticalCenter, mfapi/_MFDepthMeasurement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MFDepthMeasurement
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - _MFDepthMeasurement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFDepthMeasurement enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Specifies the measurement system for a depth value in a video frame.


## -enum-fields




### -field DistanceToFocalPlane

The measurement is the distance to the focal plane.


### -field DistanceToOpticalCenter

The measurement is the distance to the optical center.


## -remarks



Use a value from this enumeration with the <a href="mf.mf_mt_depth_measurement">MF_MT_DEPTH_MEASUREMENT</a> attribute.

The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.

<img alt="Illustration of DistanceToFocalPlane" src="images/distance_to_focal_plane.png"/>
The distance to focal center format is typically raw data from sensor such as time of flight cameras.

<img alt="Illustration of DistanceToOpticalCenter" src="images/distance_to_optical_center.png"/>


