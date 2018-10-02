---
UID: NF:vidcap.ICameraControl.getRange_ZoomRelative
title: ICameraControl::getRange_ZoomRelative
author: windows-sdk-content
description: The getRange_ZoomRelative method returns the range of relative zoom levels supported by the camera. The relative zoom indicates the direction in which the lens is moving.
old-location: dshow\icameracontrol_getrange_zoomrelative.htm
tech.root: DirectShow
ms.assetid: ea3460b8-b956-4dc9-bed7-f28714e1df11
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_ZoomRelative method, ICameraControl.getRange_ZoomRelative, ICameraControl::getRange_ZoomRelative, ICameraControlgetRange_ZoomRelative, dshow.icameracontrol_getrange_zoomrelative, getRange_ZoomRelative, getRange_ZoomRelative method [DirectShow], getRange_ZoomRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_ZoomRelative
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
 - ICameraControl.getRange_ZoomRelative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::getRange_ZoomRelative


## -description


The <code>getRange_ZoomRelative</code> method returns the range of relative zoom levels supported by the camera. The relative zoom indicates the direction in which the lens is moving.


## -parameters




### -param pMin [out]

Receives the minimum relative zoom.


### -param pMax [out]

Receives the maximum relative zoom.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default relative zoom.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

