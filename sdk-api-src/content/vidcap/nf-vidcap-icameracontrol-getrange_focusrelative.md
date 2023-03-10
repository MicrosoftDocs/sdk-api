---
UID: NF:vidcap.ICameraControl.getRange_FocusRelative
title: ICameraControl::getRange_FocusRelative (vidcap.h)
description: The getRange_FocusRelative method returns the range of relative focal distances supported by the camera. The relative focus indicates the direction in which the lens group is moving.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_FocusRelative method","ICameraControl.getRange_FocusRelative","ICameraControl::getRange_FocusRelative","ICameraControlgetRange_FocusRelative","dshow.icameracontrol_getrange_focusrelative","getRange_FocusRelative","getRange_FocusRelative method [DirectShow]","getRange_FocusRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_FocusRelative"]
old-location: dshow\icameracontrol_getrange_focusrelative.htm
tech.root: dshow
ms.assetid: c5038a59-bdc4-4034-afd1-256003687187
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_FocusRelative method, ICameraControl.getRange_FocusRelative, ICameraControl::getRange_FocusRelative, ICameraControlgetRange_FocusRelative, dshow.icameracontrol_getrange_focusrelative, getRange_FocusRelative, getRange_FocusRelative method [DirectShow], getRange_FocusRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_FocusRelative
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
 - ICameraControl::getRange_FocusRelative
 - vidcap/ICameraControl::getRange_FocusRelative
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
 - ICameraControl.getRange_FocusRelative
---

# ICameraControl::getRange_FocusRelative


## -description

The <code>getRange_FocusRelative</code> method returns the range of relative focal distances supported by the camera. The relative focus indicates the direction in which the lens group is moving.

## -parameters

### -param pMin [out]

Receives the minimum relative focus.

### -param pMax [out]

Receives the minimum relative focus.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default relative focus.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>