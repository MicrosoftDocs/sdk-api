---
UID: NF:vidcap.ICameraControl.get_Exposure
title: ICameraControl::get_Exposure (vidcap.h)
description: The get_Exposure method returns the camera's exposure time.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_Exposure method","ICameraControl.get_Exposure","ICameraControl::get_Exposure","ICameraControlget_Exposure","dshow.icameracontrol_get_exposure","get_Exposure","get_Exposure method [DirectShow]","get_Exposure method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_Exposure"]
old-location: dshow\icameracontrol_get_exposure.htm
tech.root: dshow
ms.assetid: 19323477-8dc7-46ed-b6a3-d0dd8b103924
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_Exposure method, ICameraControl.get_Exposure, ICameraControl::get_Exposure, ICameraControlget_Exposure, dshow.icameracontrol_get_exposure, get_Exposure, get_Exposure method [DirectShow], get_Exposure method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Exposure
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
 - ICameraControl::get_Exposure
 - vidcap/ICameraControl::get_Exposure
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
 - ICameraControl.get_Exposure
---

# ICameraControl::get_Exposure


## -description

The <code>get_Exposure</code> method returns the camera's exposure time.

## -parameters

### -param pValue [out]

Receives the exposure time, in log base 2 seconds. If the value is <i>n</i>, the exposure time is 2^n seconds.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>