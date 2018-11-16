---
UID: NF:vidcap.ICameraControl.getRange_TiltRelative
title: ICameraControl::getRange_TiltRelative
author: windows-sdk-content
description: The getRange_TiltRelative method returns the range of relative tilt angles supported by the camera. The relative tilt is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_getrange_tiltrelative.htm
tech.root: DirectShow
ms.assetid: 8b78e961-8b05-4339-ad66-49f2d892d4dc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_TiltRelative method, ICameraControl.getRange_TiltRelative, ICameraControl::getRange_TiltRelative, ICameraControlgetRange_TiltRelative, dshow.icameracontrol_getrange_tiltrelative, getRange_TiltRelative, getRange_TiltRelative method [DirectShow], getRange_TiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_TiltRelative
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
 - ICameraControl.getRange_TiltRelative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vidcap.h
: 
- ICameraControl.getRange_TiltRelative
: 
---

# ICameraControl::getRange_TiltRelative


## -description


The <code>getRange_TiltRelative</code> method returns the range of relative tilt angles supported by the camera. The relative tilt is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pMin [out]

Receives the minimum relative tilt angle.


### -param pMax [out]

Receives the maximum relative title angle.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default relative tilt angle.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

