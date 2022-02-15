---
UID: NE:strmif.tagCameraControlProperty
title: CameraControlProperty (strmif.h)
description: The CameraControlProperty enumeration specifies a setting on a camera.
helpviewer_keywords: ["CameraControlProperty","CameraControlProperty enumeration [DirectShow]","CameraControlPropertyEnumeration","CameraControl_Exposure","CameraControl_Focus","CameraControl_Iris","CameraControl_Pan","CameraControl_Roll","CameraControl_Tilt","CameraControl_Zoom","dshow.cameracontrolproperty","strmif/CameraControlProperty","strmif/CameraControl_Exposure","strmif/CameraControl_Focus","strmif/CameraControl_Iris","strmif/CameraControl_Pan","strmif/CameraControl_Roll","strmif/CameraControl_Tilt","strmif/CameraControl_Zoom"]
old-location: dshow\cameracontrolproperty.htm
tech.root: dshow
ms.assetid: eebf2246-960f-48ea-86b7-7542e69f2e3e
ms.date: 12/05/2018
ms.keywords: CameraControlProperty, CameraControlProperty enumeration [DirectShow], CameraControlPropertyEnumeration, CameraControl_Exposure, CameraControl_Focus, CameraControl_Iris, CameraControl_Pan, CameraControl_Roll, CameraControl_Tilt, CameraControl_Zoom, dshow.cameracontrolproperty, strmif/CameraControlProperty, strmif/CameraControl_Exposure, strmif/CameraControl_Focus, strmif/CameraControl_Iris, strmif/CameraControl_Pan, strmif/CameraControl_Roll, strmif/CameraControl_Tilt, strmif/CameraControl_Zoom
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CameraControlProperty
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCameraControlProperty
 - strmif/tagCameraControlProperty
 - CameraControlProperty
 - strmif/CameraControlProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - CameraControlProperty
---

# CameraControlProperty enumeration


## -description

The <code>CameraControlProperty</code> enumeration specifies a setting on a camera.

## -enum-fields

### -field CameraControl_Pan:0

Specifies the camera's pan setting, in degrees. Values range from –180 to +180, with the default set to zero. Positive values are clockwise from the origin (the camera rotates clockwise when viewed from above), and negative values are counterclockwise from the origin.

### -field CameraControl_Tilt

Specifies the camera's tilt setting, in degrees. Values range from –180 to +180, with the default set to zero. Positive values point the imaging plane up, and negative values point the imaging plane down.

### -field CameraControl_Roll

Specifies the camera's roll setting, in degrees. Values range from –180 to +180, with the default set to zero. Positive values cause a clockwise rotation of the camera along the image-viewing axis, and negative values cause a counterclockwise rotation of the camera.

### -field CameraControl_Zoom

Specifies the camera's zoom setting, in millimeters. Values range from 10 to 600, and the default is specific to the device.

### -field CameraControl_Exposure

Specifies the exposure setting, in log base 2 seconds. In other words, for values less than zero, the exposure time is 1/2^n seconds, and for values zero or above, the exposure time is 2^n seconds. For example:

<table>
<tr>
<th>Value
                </th>
<th>Seconds
                </th>
</tr>
<tr>
<td>-3</td>
<td>1/8</td>
</tr>
<tr>
<td>-2</td>
<td>1/4</td>
</tr>
<tr>
<td>-1</td>
<td>1/2</td>
</tr>
<tr>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>2</td>
<td>4</td>
</tr>
</table>

### -field CameraControl_Iris

Specifies the camera's iris setting, in units of fₛₜₒₚ* 10.

### -field CameraControl_Focus

Specifies the camera's focus setting, as the distance to the optimally focused target, in millimeters. The range and default value are specific to the device.

## -remarks

For a given property, a particular device might implement only a subset of the listed range.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamcameracontrol">IAMCameraControl Interface</a>
