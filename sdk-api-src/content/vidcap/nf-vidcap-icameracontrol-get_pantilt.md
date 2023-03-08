---
UID: NF:vidcap.ICameraControl.get_PanTilt
title: ICameraControl::get_PanTilt (vidcap.h)
description: The get_PanTilt method returns the camera's pan and tilt angles.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_PanTilt method","ICameraControl.get_PanTilt","ICameraControl::get_PanTilt","ICameraControlget_PanTilt","dshow.icameracontrol_get_pantilt","get_PanTilt","get_PanTilt method [DirectShow]","get_PanTilt method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_PanTilt"]
old-location: dshow\icameracontrol_get_pantilt.htm
tech.root: dshow
ms.assetid: 88f67970-2946-49f9-9c90-e562f37edd83
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_PanTilt method, ICameraControl.get_PanTilt, ICameraControl::get_PanTilt, ICameraControlget_PanTilt, dshow.icameracontrol_get_pantilt, get_PanTilt, get_PanTilt method [DirectShow], get_PanTilt method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PanTilt
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
 - ICameraControl::get_PanTilt
 - vidcap/ICameraControl::get_PanTilt
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
 - ICameraControl.get_PanTilt
---

# ICameraControl::get_PanTilt


## -description

The <code>get_PanTilt</code> method returns the camera's pan and tilt angles.

## -parameters

### -param pPanValue [out]

Receives the current panning angle, in arc seconds. An arc second is 1/3600th of a degree. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_pan">ICameraControl::get_Pan</a>.

### -param pTiltValue [out]

Receives the current tilt angle, in arc seconds. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_tilt">ICameraControl::get_Tilt</a>.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>