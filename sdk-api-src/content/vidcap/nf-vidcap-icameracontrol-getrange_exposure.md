---
UID: NF:vidcap.ICameraControl.getRange_Exposure
title: ICameraControl::getRange_Exposure (vidcap.h)
description: The getRange_Exposure method returns the range of exposure times supported by the camera.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_Exposure method","ICameraControl.getRange_Exposure","ICameraControl::getRange_Exposure","ICameraControlgetRange_Exposure","dshow.icameracontrol_getrange_exposure","getRange_Exposure","getRange_Exposure method [DirectShow]","getRange_Exposure method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_Exposure"]
old-location: dshow\icameracontrol_getrange_exposure.htm
tech.root: dshow
ms.assetid: 42e74ae3-6a07-47c8-8e6a-daf2cb32328c
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_Exposure method, ICameraControl.getRange_Exposure, ICameraControl::getRange_Exposure, ICameraControlgetRange_Exposure, dshow.icameracontrol_getrange_exposure, getRange_Exposure, getRange_Exposure method [DirectShow], getRange_Exposure method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Exposure
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
 - ICameraControl::getRange_Exposure
 - vidcap/ICameraControl::getRange_Exposure
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
 - ICameraControl.getRange_Exposure
---

# ICameraControl::getRange_Exposure


## -description

The <code>getRange_Exposure</code> method returns the range of exposure times supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum exposure time, in log base 2 seconds. If the value is <i>n</i>, the exposure time is 2^n seconds.

### -param pMax [out]

Receives the maximum exposure time, in log base 2 seconds.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default exposure time.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>