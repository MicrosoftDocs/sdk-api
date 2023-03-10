---
UID: NF:vidcap.ICameraControl.get_Pan
title: ICameraControl::get_Pan (vidcap.h)
description: The get_Pan method returns the camera's panning angle.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_Pan method","ICameraControl.get_Pan","ICameraControl::get_Pan","ICameraControlget_Pan","dshow.icameracontrol_get_pan","get_Pan","get_Pan method [DirectShow]","get_Pan method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_Pan"]
old-location: dshow\icameracontrol_get_pan.htm
tech.root: dshow
ms.assetid: 4cbf7582-63ad-4572-be62-be1fe5bc60b3
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_Pan method, ICameraControl.get_Pan, ICameraControl::get_Pan, ICameraControlget_Pan, dshow.icameracontrol_get_pan, get_Pan, get_Pan method [DirectShow], get_Pan method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Pan
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
 - ICameraControl::get_Pan
 - vidcap/ICameraControl::get_Pan
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
 - ICameraControl.get_Pan
---

# ICameraControl::get_Pan


## -description

The <code>get_Pan</code> method returns the camera's panning angle.

## -parameters

### -param pValue [out]

Receives the panning angle, in degrees. Positive values are clockwise when viewing the camera from above, and negative values are counter clockwise. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_pan">ICameraControl::getRange_Pan</a>.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>