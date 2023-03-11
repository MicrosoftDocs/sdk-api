---
UID: NE:strmif.tagCameraControlFlags
title: CameraControlFlags (strmif.h)
description: The CameraControlFlags enumeration defines whether a camera setting is controlled manually or automatically.
helpviewer_keywords: ["CameraControlFlags","CameraControlFlags enumeration [DirectShow]","CameraControlFlagsEnumeration","CameraControl_Flags_Auto","CameraControl_Flags_Manual","dshow.cameracontrolflags","strmif/CameraControlFlags","strmif/CameraControl_Flags_Auto","strmif/CameraControl_Flags_Manual"]
old-location: dshow\cameracontrolflags.htm
tech.root: dshow
ms.assetid: 806322e7-9a70-4dc1-8b10-2479fb3ec935
ms.date: 12/05/2018
ms.keywords: CameraControlFlags, CameraControlFlags enumeration [DirectShow], CameraControlFlagsEnumeration, CameraControl_Flags_Auto, CameraControl_Flags_Manual, dshow.cameracontrolflags, strmif/CameraControlFlags, strmif/CameraControl_Flags_Auto, strmif/CameraControl_Flags_Manual
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
req.typenames: CameraControlFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCameraControlFlags
 - strmif/tagCameraControlFlags
 - CameraControlFlags
 - strmif/CameraControlFlags
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
 - CameraControlFlags
---

# CameraControlFlags enumeration


## -description

The <b>CameraControlFlags</b> enumeration defines whether a camera setting is controlled manually or automatically.

## -enum-fields

### -field CameraControl_Flags_Auto:0x1

The setting is controlled automatically.

### -field CameraControl_Flags_Manual:0x2

The setting is controlled manually.

## -remarks

In addition, the following flags are defined in Ksmedia.h:

<table>
<tr>
<th>Flag</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>KSPROPERTY_CAMERACONTROL_FLAGS_AUTO</b></td>
<td>0X0001L</td>
<td>Equivalent to CameraControl_Flags_Auto.</td>
</tr>
<tr>
<td><b>KSPROPERTY_CAMERACONTROL_FLAGS_MANUAL</b></td>
<td>0X0002L</td>
<td>Equivalent to CameraControl_Flags_Manual.</td>
</tr>
<tr>
<td><b>KSPROPERTY_CAMERACONTROL_FLAGS_ABSOLUTE</b></td>
<td>0X0000L</td>
<td>The camera supports absolute units for this setting.</td>
</tr>
<tr>
<td><b>KSPROPERTY_CAMERACONTROL_FLAGS_RELATIVE</b></td>
<td>0X0010L</td>
<td>The camera supports relative controls for this setting. A relative control is divided into a number of steps with no defined units. The absolute size of each step depends on the camera model.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamcameracontrol">IAMCameraControl Interface</a>
