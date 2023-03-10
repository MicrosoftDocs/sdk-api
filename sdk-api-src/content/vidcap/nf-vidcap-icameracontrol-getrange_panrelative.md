---
UID: NF:vidcap.ICameraControl.getRange_PanRelative
title: ICameraControl::getRange_PanRelative (vidcap.h)
description: The getRange_PanRelative method returns the range of relative panning angles supported by the camera. The relative pan is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_PanRelative method","ICameraControl.getRange_PanRelative","ICameraControl::getRange_PanRelative","ICameraControlgetRange_PanRelative","dshow.icameracontrol_getrange_panrelative","getRange_PanRelative","getRange_PanRelative method [DirectShow]","getRange_PanRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_PanRelative"]
old-location: dshow\icameracontrol_getrange_panrelative.htm
tech.root: dshow
ms.assetid: 31affca6-e9e9-4715-aea4-0a39ce100556
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_PanRelative method, ICameraControl.getRange_PanRelative, ICameraControl::getRange_PanRelative, ICameraControlgetRange_PanRelative, dshow.icameracontrol_getrange_panrelative, getRange_PanRelative, getRange_PanRelative method [DirectShow], getRange_PanRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_PanRelative
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
 - ICameraControl::getRange_PanRelative
 - vidcap/ICameraControl::getRange_PanRelative
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
 - ICameraControl.getRange_PanRelative
---

# ICameraControl::getRange_PanRelative


## -description

The <code>getRange_PanRelative</code> method returns the range of relative panning angles supported by the camera. The relative pan is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param pMin [out]

Receives the minimum relative panning angle.

### -param pMax [out]

Receives the maximum relative panning angle.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default relative panning angle.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>