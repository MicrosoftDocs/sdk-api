---
UID: NF:vidcap.ICameraControl.get_ZoomRelative
title: ICameraControl::get_ZoomRelative (vidcap.h)
description: The get_ZoomRelative method returns the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_ZoomRelative method","ICameraControl.get_ZoomRelative","ICameraControl::get_ZoomRelative","ICameraControlget_ZoomRelative","dshow.icameracontrol_get_zoomrelative","get_ZoomRelative","get_ZoomRelative method [DirectShow]","get_ZoomRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_ZoomRelative"]
old-location: dshow\icameracontrol_get_zoomrelative.htm
tech.root: dshow
ms.assetid: c1926541-d7c7-4a16-bbe7-0d93dec89c67
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_ZoomRelative method, ICameraControl.get_ZoomRelative, ICameraControl::get_ZoomRelative, ICameraControlget_ZoomRelative, dshow.icameracontrol_get_zoomrelative, get_ZoomRelative, get_ZoomRelative method [DirectShow], get_ZoomRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_ZoomRelative
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
 - ICameraControl::get_ZoomRelative
 - vidcap/ICameraControl::get_ZoomRelative
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
 - ICameraControl.get_ZoomRelative
---

# ICameraControl::get_ZoomRelative


## -description

The <code>get_ZoomRelative</code> method returns the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.

## -parameters

### -param pValue [out]

Receives the relative zoom. The size of the value represents the desired zoom speed; a higher value represents a higher speed. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_zoomrelative">ICameraControl::getRange_ZoomRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Stopped.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Zoom lens moving in the telephoto direction.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Zoom lens moving in the wide angle direction.</td>
</tr>
</table>

### -param pFlags [out]

Receives one or more flags. See <a href="/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>