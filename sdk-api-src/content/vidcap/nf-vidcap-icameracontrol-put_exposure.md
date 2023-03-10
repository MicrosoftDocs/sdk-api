---
UID: NF:vidcap.ICameraControl.put_Exposure
title: ICameraControl::put_Exposure (vidcap.h)
description: The put_Exposure method sets the camera's exposure time.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_Exposure method","ICameraControl.put_Exposure","ICameraControl::put_Exposure","ICameraControlput_Exposure","dshow.icameracontrol_put_exposure","put_Exposure","put_Exposure method [DirectShow]","put_Exposure method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_Exposure"]
old-location: dshow\icameracontrol_put_exposure.htm
tech.root: dshow
ms.assetid: 2db9bdb3-c508-40b6-bd5e-75e418ba2f18
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_Exposure method, ICameraControl.put_Exposure, ICameraControl::put_Exposure, ICameraControlput_Exposure, dshow.icameracontrol_put_exposure, put_Exposure, put_Exposure method [DirectShow], put_Exposure method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Exposure
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
 - ICameraControl::put_Exposure
 - vidcap/ICameraControl::put_Exposure
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
 - ICameraControl.put_Exposure
---

# ICameraControl::put_Exposure


## -description

The <code>put_Exposure</code> method sets the camera's exposure time.

## -parameters

### -param Value [in]

Exposure time, in log base 2 seconds. If the value is <i>n</i>, the exposure time is 2^n seconds.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>