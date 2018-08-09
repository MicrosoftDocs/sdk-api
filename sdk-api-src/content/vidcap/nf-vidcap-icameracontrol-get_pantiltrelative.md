---
UID: NF:vidcap.ICameraControl.get_PanTiltRelative
title: ICameraControl::get_PanTiltRelative
author: windows-sdk-content
description: The get_PanTiltRelative method returns the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_get_pantiltrelative.htm
old-project: DirectShow
ms.assetid: 5d96dcfb-c0c4-4521-bf1f-30947577d305
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: ICameraControl interface [DirectShow],get_PanTiltRelative method, ICameraControl.get_PanTiltRelative, ICameraControl::get_PanTiltRelative, ICameraControlget_PanTiltRelative, dshow.icameracontrol_get_pantiltrelative, get_PanTiltRelative, get_PanTiltRelative method [DirectShow], get_PanTiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PanTiltRelative
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
 - ICameraControl.get_PanTiltRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_PanTiltRelative


## -description


The <code>get_PanTiltRelative</code> method returns the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pPanValue [out]

Receives the relative pan. See <a href="https://msdn.microsoft.com/a7237e0a-82b3-4e2a-a6c7-97fbb03b5917">ICameraControl::get_PanRelative</a>.
          


### -param pTiltValue [out]

Receives the relative tilt. See <a href="https://msdn.microsoft.com/e8730043-a506-4c74-a9ca-94d6e003a4b1">ICameraControl::get_TiltRelative</a>.
          


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.
          


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

