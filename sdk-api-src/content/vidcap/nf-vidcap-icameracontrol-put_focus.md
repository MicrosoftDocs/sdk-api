---
UID: NF:vidcap.ICameraControl.put_Focus
title: ICameraControl::put_Focus (vidcap.h)
description: The put_Focus method sets the distance that is optimally in focus.helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_Focus method","ICameraControl.put_Focus","ICameraControl::put_Focus","ICameraControlput_Focus","dshow.icameracontrol_put_focus","put_Focus","put_Focus method [DirectShow]","put_Focus method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_Focus"]
old-location: dshow\icameracontrol_put_focus.htm
tech.root: DirectShow
ms.assetid: c896bf2b-33b6-4e7c-bf84-b7dd8f57a4d4
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_Focus method, ICameraControl.put_Focus, ICameraControl::put_Focus, ICameraControlput_Focus, dshow.icameracontrol_put_focus, put_Focus, put_Focus method [DirectShow], put_Focus method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Focus
f1_keywords:
- vidcap/ICameraControl.put_Focus
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
- ICameraControl.put_Focus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::put_Focus


## -description


The <code>put_Focus</code> method sets the distance that is optimally in focus.


## -parameters




### -param Value [in]

Specifies the focus distance, in millimeters.


### -param Flags [in]

Zero or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

