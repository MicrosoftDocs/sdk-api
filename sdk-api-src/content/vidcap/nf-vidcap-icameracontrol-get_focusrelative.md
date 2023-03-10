---
UID: NF:vidcap.ICameraControl.get_FocusRelative
title: ICameraControl::get_FocusRelative (vidcap.h)
description: The get_FocusRelative method returns the relative focus. The relative focus indicates the direction in which the lens group is moving.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_FocusRelative method","ICameraControl.get_FocusRelative","ICameraControl::get_FocusRelative","ICameraControlget_FocusRelative","dshow.icameracontrol_get_focusrelative","get_FocusRelative","get_FocusRelative method [DirectShow]","get_FocusRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_FocusRelative"]
old-location: dshow\icameracontrol_get_focusrelative.htm
tech.root: dshow
ms.assetid: 21bc1cbe-747b-4846-814f-1aed0ac614d6
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_FocusRelative method, ICameraControl.get_FocusRelative, ICameraControl::get_FocusRelative, ICameraControlget_FocusRelative, dshow.icameracontrol_get_focusrelative, get_FocusRelative, get_FocusRelative method [DirectShow], get_FocusRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_FocusRelative
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
 - ICameraControl::get_FocusRelative
 - vidcap/ICameraControl::get_FocusRelative
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
 - ICameraControl.get_FocusRelative
---

# ICameraControl::get_FocusRelative


## -description

The <code>get_FocusRelative</code> method returns the relative focus. The relative focus indicates the direction in which the lens group is moving.

## -parameters

### -param pValue [out]

Receives the relative focus. The size of the value represents the speed at which the focal point changes; a higher value represents a higher speed. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_focusrelative">ICameraControl::getRange_FocusRelative</a>.

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
<td>Focus is moving closer to the object.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Focus is moving farther away from the object.</td>
</tr>
</table>

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>