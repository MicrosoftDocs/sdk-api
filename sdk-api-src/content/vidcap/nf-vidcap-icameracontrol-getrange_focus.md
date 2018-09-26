---
UID: NF:vidcap.ICameraControl.getRange_Focus
title: ICameraControl::getRange_Focus
author: windows-sdk-content
description: The getRange_Focus method returns the range of focal distances supported by the camera.
old-location: dshow\icameracontrol_getrange_focus.htm
tech.root: DirectShow
ms.assetid: f2da5473-82c3-4719-bba6-04a1793a98eb
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_Focus method, ICameraControl.getRange_Focus, ICameraControl::getRange_Focus, ICameraControlgetRange_Focus, dshow.icameracontrol_getrange_focus, getRange_Focus, getRange_Focus method [DirectShow], getRange_Focus method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Focus
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICameraControl.getRange_Focus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::getRange_Focus


## -description


The <code>getRange_Focus</code> method returns the range of focal distances supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum focus distance, in millimeters.


### -param pMax [out]

Receives the maximum focus distance, in millimeters.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default focus distance.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

