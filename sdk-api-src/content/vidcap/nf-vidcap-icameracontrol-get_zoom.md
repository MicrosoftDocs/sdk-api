---
UID: NF:vidcap.ICameraControl.get_Zoom
title: ICameraControl::get_Zoom (vidcap.h)
description: The get_Zoom method returns the camera's optical zoom level.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_Zoom method","ICameraControl.get_Zoom","ICameraControl::get_Zoom","ICameraControlget_Zoom","dshow.icameracontrol_get_zoom","get_Zoom","get_Zoom method [DirectShow]","get_Zoom method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_Zoom"]
old-location: dshow\icameracontrol_get_zoom.htm
tech.root: dshow
ms.assetid: 7c1fe500-bccf-46ed-bcd9-f65b25e8ccb7
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_Zoom method, ICameraControl.get_Zoom, ICameraControl::get_Zoom, ICameraControlget_Zoom, dshow.icameracontrol_get_zoom, get_Zoom, get_Zoom method [DirectShow], get_Zoom method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Zoom
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
 - ICameraControl::get_Zoom
 - vidcap/ICameraControl::get_Zoom
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
 - ICameraControl.get_Zoom
---

# ICameraControl::get_Zoom


## -description

The <code>get_Zoom</code> method returns the camera's optical zoom level.

## -parameters

### -param pValue [out]

Receives the zoom level. The units for this setting are not defined. For information about calculating magnification from zoom level, see <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_focallengths">ICameraControl::get_FocalLengths</a>.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns the optical zoom level only. To get the digital zoom level, call <a href="/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_digitalmultiplier">IVideoProcAmp::get_DigitalMultiplier</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>