---
UID: NF:vidcap.ICameraControl.get_Roll
title: ICameraControl::get_Roll (vidcap.h)
description: .helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_Roll method","ICameraControl.get_Roll","ICameraControl::get_Roll","ICameraControlget_Roll","dshow.icameracontrol_get_roll","get_Roll","get_Roll method [DirectShow]","get_Roll method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_Roll"]
old-location: dshow\icameracontrol_get_roll.htm
tech.root: DirectShow
ms.assetid: cebe99e1-9bcc-4826-8b15-b4d6757ec5b4
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_Roll method, ICameraControl.get_Roll, ICameraControl::get_Roll, ICameraControlget_Roll, dshow.icameracontrol_get_roll, get_Roll, get_Roll method [DirectShow], get_Roll method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Roll
f1_keywords:
- vidcap/ICameraControl.get_Roll
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
- ICameraControl.get_Roll
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_Roll


## -description




The <code>get_Roll</code> method returns the camera's roll angle.


## -parameters




### -param pValue [out]

Receives the roll angle, in degrees. Positive values are clockwise along the image viewing axis, and negative values are counter clockwise. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_roll">ICameraControl::getRange_Roll</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

