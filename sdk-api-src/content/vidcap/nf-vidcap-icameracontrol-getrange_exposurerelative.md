---
UID: NF:vidcap.ICameraControl.getRange_ExposureRelative
title: ICameraControl::getRange_ExposureRelative
author: windows-sdk-content
description: The getRange_ExposureRelative method returns the range of relative exposure times supported by the camera. The relative exposure time is expressed as a number of steps, where the absolute value of each step depends on the camera model.
old-location: dshow\icameracontrol_getrange_exposurerelative.htm
old-project: DirectShow
ms.assetid: ab46e893-037a-42bb-a3ae-bef943cd6a5e
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_ExposureRelative method, ICameraControl.getRange_ExposureRelative, ICameraControl::getRange_ExposureRelative, ICameraControlgetRange_ExposureRelative, dshow.icameracontrol_getrange_exposurerelative, getRange_ExposureRelative, getRange_ExposureRelative method [DirectShow], getRange_ExposureRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_ExposureRelative
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.redist: 
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
 - ICameraControl.getRange_ExposureRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::getRange_ExposureRelative


## -description


The <code>getRange_ExposureRelative</code> method returns the range of relative exposure times supported by the camera. The relative exposure time is expressed as a number of steps, where the absolute value of each step depends on the camera model.


## -parameters




### -param pMin [out]

Receives the minimum relative exposure time.


### -param pMax [out]

Receives the maximum relative exposure time.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default relative exposure time.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

