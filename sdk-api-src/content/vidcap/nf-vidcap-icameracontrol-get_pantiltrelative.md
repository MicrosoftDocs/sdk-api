---
UID: NF:vidcap.ICameraControl.get_PanTiltRelative
title: ICameraControl::get_PanTiltRelative (vidcap.h)
author: windows-sdk-content
description: The get_PanTiltRelative method returns the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_get_pantiltrelative.htm
tech.root: DirectShow
ms.assetid: 5d96dcfb-c0c4-4521-bf1f-30947577d305
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_PanTiltRelative method, ICameraControl.get_PanTiltRelative, ICameraControl::get_PanTiltRelative, ICameraControlget_PanTiltRelative, dshow.icameracontrol_get_pantiltrelative, get_PanTiltRelative, get_PanTiltRelative method [DirectShow], get_PanTiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PanTiltRelative
ms.topic: method
f1_keywords: 
 - "vidcap/ICameraControl.get_PanTiltRelative"
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
 - ICameraControl.get_PanTiltRelative
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_PanTiltRelative


## -description


The <code>get_PanTiltRelative</code> method returns the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pPanValue [out]

Receives the relative pan. See <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_panrelative">ICameraControl::get_PanRelative</a>.
          


### -param pTiltValue [out]

Receives the relative tilt. See <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_tiltrelative">ICameraControl::get_TiltRelative</a>.
          


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.
          


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

