---
UID: NF:vidcap.ICameraControl.get_Iris
title: ICameraControl::get_Iris (vidcap.h)
description: The get_Iris method returns the camera's aperture setting.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_Iris method","ICameraControl.get_Iris","ICameraControl::get_Iris","ICameraControlget_Iris","dshow.icameracontrol_get_iris","get_Iris","get_Iris method [DirectShow]","get_Iris method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_Iris"]
old-location: dshow\icameracontrol_get_iris.htm
tech.root: dshow
ms.assetid: 710a29f1-f5ab-42cf-b912-dd9b4546757e
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_Iris method, ICameraControl.get_Iris, ICameraControl::get_Iris, ICameraControlget_Iris, dshow.icameracontrol_get_iris, get_Iris, get_Iris method [DirectShow], get_Iris method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Iris
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
 - ICameraControl::get_Iris
 - vidcap/ICameraControl::get_Iris
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
 - ICameraControl.get_Iris
---

# ICameraControl::get_Iris


## -description

The <code>get_Iris</code> method returns the camera's aperture setting.

## -parameters

### -param pValue [out]

Receives the aperture setting, in units of f-stop * 10.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>