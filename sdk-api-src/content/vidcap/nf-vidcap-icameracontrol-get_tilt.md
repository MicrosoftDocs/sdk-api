---
UID: NF:vidcap.ICameraControl.get_Tilt
title: ICameraControl::get_Tilt (vidcap.h)
description: The get_Tilt method returns the camera's tilt angle.helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_Tilt method","ICameraControl.get_Tilt","ICameraControl::get_Tilt","ICameraControlget_Tilt","dshow.icameracontrol_get_tilt","get_Tilt","get_Tilt method [DirectShow]","get_Tilt method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_Tilt"]
old-location: dshow\icameracontrol_get_tilt.htm
tech.root: DirectShow
ms.assetid: 8e9d9176-fb27-4221-876b-49f407289877
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_Tilt method, ICameraControl.get_Tilt, ICameraControl::get_Tilt, ICameraControlget_Tilt, dshow.icameracontrol_get_tilt, get_Tilt, get_Tilt method [DirectShow], get_Tilt method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Tilt
f1_keywords:
- vidcap/ICameraControl.get_Tilt
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- ICameraControl.get_Tilt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_Tilt


## -description


The <code>get_Tilt</code> method returns the camera's tilt angle.


## -parameters




### -param pValue [out]

Receives the tilt angle, in degrees. Positive values point the camera up, and negative values point the camera down. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_tilt">ICameraControl::getRange_Tilt</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

