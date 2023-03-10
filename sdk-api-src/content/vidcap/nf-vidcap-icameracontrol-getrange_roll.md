---
UID: NF:vidcap.ICameraControl.getRange_Roll
title: ICameraControl::getRange_Roll (vidcap.h)
description: The getRange_Roll method returns the range of roll angles supported by the camera.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_Roll method","ICameraControl.getRange_Roll","ICameraControl::getRange_Roll","ICameraControlgetRange_Roll","dshow.icameracontrol_getrange_roll","getRange_Roll","getRange_Roll method [DirectShow]","getRange_Roll method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_Roll"]
old-location: dshow\icameracontrol_getrange_roll.htm
tech.root: dshow
ms.assetid: 14400765-d8a2-4ac2-a26b-39949ecd2bda
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_Roll method, ICameraControl.getRange_Roll, ICameraControl::getRange_Roll, ICameraControlgetRange_Roll, dshow.icameracontrol_getrange_roll, getRange_Roll, getRange_Roll method [DirectShow], getRange_Roll method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Roll
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
 - ICameraControl::getRange_Roll
 - vidcap/ICameraControl::getRange_Roll
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
 - ICameraControl.getRange_Roll
---

# ICameraControl::getRange_Roll


## -description

The <code>getRange_Roll</code> method returns the range of roll angles supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum roll angle, in degrees.

### -param pMax [out]

Receives the maximum roll angle, in degrees.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default roll angle, in degrees.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>