---
UID: NF:vidcap.ICameraControl.getRange_Zoom
title: ICameraControl::getRange_Zoom
author: windows-sdk-content
description: The getRange_Zoom method returns the range of zoom levels supported by the camera.
old-location: dshow\icameracontrol_getrange_zoom.htm
tech.root: DirectShow
ms.assetid: 93a81b65-4b63-45c9-b065-f4aa5cf2e4ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_Zoom method, ICameraControl.getRange_Zoom, ICameraControl::getRange_Zoom, ICameraControlgetRange_Zoom, dshow.icameracontrol_getrange_zoom, getRange_Zoom, getRange_Zoom method [DirectShow], getRange_Zoom method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Zoom
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
 - ICameraControl.getRange_Zoom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::getRange_Zoom


## -description


The <code>getRange_Zoom</code> method returns the range of zoom levels supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum zoom.


### -param pMax [out]

Receives the maximum zoom.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default zoom.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



For information about calculating magnification from zoom level, see <a href="https://msdn.microsoft.com/de566705-1f4b-4ffa-932d-a52521e6963b">ICameraControl::get_FocalLengths</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

