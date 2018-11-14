---
UID: NF:vidcap.ICameraControl.getRange_IrisRelative
title: ICameraControl::getRange_IrisRelative
author: windows-sdk-content
description: The getRange_IrisRelative method returns the range of relative aperture settings supported by the camera. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_getrange_irisrelative.htm
tech.root: DirectShow
ms.assetid: 9816e29b-3366-49e7-aa4c-46b06963c176
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_IrisRelative method, ICameraControl.getRange_IrisRelative, ICameraControl::getRange_IrisRelative, ICameraControlgetRange_IrisRelative, dshow.icameracontrol_getrange_irisrelative, getRange_IrisRelative, getRange_IrisRelative method [DirectShow], getRange_IrisRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_IrisRelative
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
 - ICameraControl.getRange_IrisRelative
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
- ICameraControl.getRange_IrisRelative
: 
---

# ICameraControl::getRange_IrisRelative


## -description


The <code>getRange_IrisRelative</code> method returns the range of relative aperture settings supported by the camera. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pMin [out]

Receives the minimum relative aperture setting.


### -param pMax [out]

Receives the maximum relative aperture setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default relative aperture setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

