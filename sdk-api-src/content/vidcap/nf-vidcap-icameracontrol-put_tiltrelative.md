---
UID: NF:vidcap.ICameraControl.put_TiltRelative
title: ICameraControl::put_TiltRelative (vidcap.h)
description: The put_TiltRelative method sets the camera's relative tilt. The relative tilt is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_TiltRelative method","ICameraControl.put_TiltRelative","ICameraControl::put_TiltRelative","ICameraControlput_TiltRelative","dshow.icameracontrol_put_tiltrelative","put_TiltRelative","put_TiltRelative method [DirectShow]","put_TiltRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_TiltRelative"]
old-location: dshow\icameracontrol_put_tiltrelative.htm
tech.root: dshow
ms.assetid: 69aa7ecf-4816-460b-b4f8-480c0d4f8331
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_TiltRelative method, ICameraControl.put_TiltRelative, ICameraControl::put_TiltRelative, ICameraControlput_TiltRelative, dshow.icameracontrol_put_tiltrelative, put_TiltRelative, put_TiltRelative method [DirectShow], put_TiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_TiltRelative
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICameraControl::put_TiltRelative
 - vidcap/ICameraControl::put_TiltRelative
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl.put_TiltRelative
---

# ICameraControl::put_TiltRelative


## -description

The <code>put_TiltRelative</code> method sets the camera's relative tilt. The relative tilt is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param Value [in]

Specifies the relative tilt. The size of the value represents the desired tilt speed; a higher value represents a higher speed. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_tiltrelative">ICameraControl::getRange_TiltRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Stop tilting.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Start tilting up.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Start tilting down.</td>
</tr>
</table>

### -param Flags [in]

Zero or more flags. See <a href="/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>