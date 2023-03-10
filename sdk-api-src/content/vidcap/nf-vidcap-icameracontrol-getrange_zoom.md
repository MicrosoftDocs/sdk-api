---
UID: NF:vidcap.ICameraControl.getRange_Zoom
title: ICameraControl::getRange_Zoom (vidcap.h)
description: The getRange_Zoom method returns the range of zoom levels supported by the camera.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_Zoom method","ICameraControl.getRange_Zoom","ICameraControl::getRange_Zoom","ICameraControlgetRange_Zoom","dshow.icameracontrol_getrange_zoom","getRange_Zoom","getRange_Zoom method [DirectShow]","getRange_Zoom method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_Zoom"]
old-location: dshow\icameracontrol_getrange_zoom.htm
tech.root: dshow
ms.assetid: 93a81b65-4b63-45c9-b065-f4aa5cf2e4ae
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_Zoom method, ICameraControl.getRange_Zoom, ICameraControl::getRange_Zoom, ICameraControlgetRange_Zoom, dshow.icameracontrol_getrange_zoom, getRange_Zoom, getRange_Zoom method [DirectShow], getRange_Zoom method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Zoom
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
 - ICameraControl::getRange_Zoom
 - vidcap/ICameraControl::getRange_Zoom
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
 - ICameraControl.getRange_Zoom
---

# ICameraControl::getRange_Zoom


## -description

The <code>getRange_Zoom</code> method returns the range of zoom levels supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum zoom.

### -param pMax [out]

Receives the maximum zoom.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default zoom.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

For information about calculating magnification from zoom level, see <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_focallengths">ICameraControl::get_FocalLengths</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>