---
UID: NF:vidcap.ICameraControl.put_Iris
title: ICameraControl::put_Iris (vidcap.h)
description: The put_Iris method sets the camera's aperture setting.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_Iris method","ICameraControl.put_Iris","ICameraControl::put_Iris","ICameraControlput_Iris","dshow.icameracontrol_put_iris","put_Iris","put_Iris method [DirectShow]","put_Iris method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_Iris"]
old-location: dshow\icameracontrol_put_iris.htm
tech.root: dshow
ms.assetid: b181f556-3d3d-4622-8cc9-57fda50bf9c0
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_Iris method, ICameraControl.put_Iris, ICameraControl::put_Iris, ICameraControlput_Iris, dshow.icameracontrol_put_iris, put_Iris, put_Iris method [DirectShow], put_Iris method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Iris
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
 - ICameraControl::put_Iris
 - vidcap/ICameraControl::put_Iris
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
 - ICameraControl.put_Iris
---

# ICameraControl::put_Iris


## -description

The <code>put_Iris</code> method sets the camera's aperture setting.

## -parameters

### -param Value [in]

Specifies the aperture setting, in units of f-stop * 10.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>