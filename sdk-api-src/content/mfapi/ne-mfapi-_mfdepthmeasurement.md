---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



Use a value from this enumeration with the <a href="https://msdn.microsoft.com/7BFA846B-E614-4117-A196-298E065CB7F8">MF_MT_DEPTH_MEASUREMENT</a> attribute.

The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.

<img alt="Illustration of DistanceToFocalPlane" src="images/distance_to_focal_plane.png"/>
The distance to focal center format is typically raw data from sensor such as time of flight cameras.

<img alt="Illustration of DistanceToOpticalCenter" src="images/distance_to_optical_center.png"/>


