---
UID: NF:vidcap.ICameraControl.get_PanTilt
title: ICameraControl::get_PanTilt
author: windows-sdk-content
description: The get_PanTilt method returns the camera's pan and tilt angles.
old-location: dshow\icameracontrol_get_pantilt.htm
old-project: DirectShow
ms.assetid: 88f67970-2946-49f9-9c90-e562f37edd83
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ICameraControl interface [DirectShow],get_PanTilt method, ICameraControl.get_PanTilt, ICameraControl::get_PanTilt, ICameraControlget_PanTilt, dshow.icameracontrol_get_pantilt, get_PanTilt, get_PanTilt method [DirectShow], get_PanTilt method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PanTilt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl.get_PanTilt
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_PanTilt


## -description


The <code>get_PanTilt</code> method returns the camera's pan and tilt angles.


## -parameters




### -param pPanValue [out]

Receives the current panning angle, in arc seconds. An arc second is 1/3600th of a degree. See <a href="https://msdn.microsoft.com/4cbf7582-63ad-4572-be62-be1fe5bc60b3">ICameraControl::get_Pan</a>.


### -param pTiltValue [out]

Receives the current tilt angle, in arc seconds. See <a href="https://msdn.microsoft.com/8e9d9176-fb27-4221-876b-49f407289877">ICameraControl::get_Tilt</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

