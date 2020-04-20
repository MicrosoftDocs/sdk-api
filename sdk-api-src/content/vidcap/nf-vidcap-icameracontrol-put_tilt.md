---
UID: NF:vidcap.ICameraControl.put_Tilt
title: ICameraControl::put_Tilt (vidcap.h)
description: The put_Tilt method sets the camera's tilt angle.helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_Tilt method","ICameraControl.put_Tilt","ICameraControl::put_Tilt","ICameraControlput_Tilt","dshow.icameracontrol_put_tilt","put_Tilt","put_Tilt method [DirectShow]","put_Tilt method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_Tilt"]
old-location: dshow\icameracontrol_put_tilt.htm
tech.root: DirectShow
ms.assetid: e75adedb-5cf2-4b2c-bb57-1bfedfc81979
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_Tilt method, ICameraControl.put_Tilt, ICameraControl::put_Tilt, ICameraControlput_Tilt, dshow.icameracontrol_put_tilt, put_Tilt, put_Tilt method [DirectShow], put_Tilt method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Tilt
f1_keywords:
- vidcap/ICameraControl.put_Tilt
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
- ICameraControl.put_Tilt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::put_Tilt


## -description


The <code>put_Tilt</code> method sets the camera's tilt angle.


## -parameters




### -param Value [in]

Specifies the tilt angle, in degrees. Positive values point the camera up, and negative values point the camera down. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_tilt">ICameraControl::getRange_Tilt</a>.


### -param Flags [in]

Zero or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

