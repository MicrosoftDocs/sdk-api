---
UID: NF:vidcap.ICameraControl.put_PanTiltRelative
title: ICameraControl::put_PanTiltRelative (vidcap.h)
description: The put_PanTiltRelative method sets the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_PanTiltRelative method","ICameraControl.put_PanTiltRelative","ICameraControl::put_PanTiltRelative","ICameraControlput_PanTiltRelative","dshow.icameracontrol_put_pantiltrelative","put_PanTiltRelative","put_PanTiltRelative method [DirectShow]","put_PanTiltRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_PanTiltRelative"]
old-location: dshow\icameracontrol_put_pantiltrelative.htm
tech.root: dshow
ms.assetid: 69d8303c-2ff2-416d-909c-e9f352e53cf1
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_PanTiltRelative method, ICameraControl.put_PanTiltRelative, ICameraControl::put_PanTiltRelative, ICameraControlput_PanTiltRelative, dshow.icameracontrol_put_pantiltrelative, put_PanTiltRelative, put_PanTiltRelative method [DirectShow], put_PanTiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_PanTiltRelative
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
 - ICameraControl::put_PanTiltRelative
 - vidcap/ICameraControl::put_PanTiltRelative
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
 - ICameraControl.put_PanTiltRelative
---

# ICameraControl::put_PanTiltRelative


## -description

The <code>put_PanTiltRelative</code> method sets the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param PanValue [in]

Specifies the relative pan. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_panrelative">ICameraControl::put_PanRelative</a>.

### -param TiltValue [in]

Specifies the relative tilt. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_tiltrelative">ICameraControl::put_TiltRelative</a>.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>