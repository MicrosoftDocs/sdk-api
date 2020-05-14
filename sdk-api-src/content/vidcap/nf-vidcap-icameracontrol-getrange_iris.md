---
UID: NF:vidcap.ICameraControl.getRange_Iris
title: ICameraControl::getRange_Iris (vidcap.h)
description: The getRange_Iris method returns the range of aperture settings supported by the camera.helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_Iris method","ICameraControl.getRange_Iris","ICameraControl::getRange_Iris","ICameraControlgetRange_Iris","dshow.icameracontrol_getrange_iris","getRange_Iris","getRange_Iris method [DirectShow]","getRange_Iris method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_Iris"]
old-location: dshow\icameracontrol_getrange_iris.htm
tech.root: DirectShow
ms.assetid: 3f3bc5b0-18eb-470c-9922-1d401f43e269
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_Iris method, ICameraControl.getRange_Iris, ICameraControl::getRange_Iris, ICameraControlgetRange_Iris, dshow.icameracontrol_getrange_iris, getRange_Iris, getRange_Iris method [DirectShow], getRange_Iris method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Iris
f1_keywords:
- vidcap/ICameraControl.getRange_Iris
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
- ICameraControl.getRange_Iris
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::getRange_Iris


## -description


The <code>getRange_Iris</code> method returns the range of aperture settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum aperture setting, in units of f-stop * 100.


### -param pMax [out]

Receives the maximum aperture setting, in units of f-stop * 100.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default aperture setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

