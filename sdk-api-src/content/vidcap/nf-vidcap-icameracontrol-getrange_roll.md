---
UID: NF:vidcap.ICameraControl.getRange_Roll
title: ICameraControl::getRange_Roll
author: windows-sdk-content
description: The getRange_Roll method returns the range of roll angles supported by the camera.
old-location: dshow\icameracontrol_getrange_roll.htm
old-project: DirectShow
ms.assetid: 14400765-d8a2-4ac2-a26b-39949ecd2bda
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_Roll method, ICameraControl.getRange_Roll, ICameraControl::getRange_Roll, ICameraControlgetRange_Roll, dshow.icameracontrol_getrange_roll, getRange_Roll, getRange_Roll method [DirectShow], getRange_Roll method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Roll
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
 - ICameraControl.getRange_Roll
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::getRange_Roll


## -description


The <code>getRange_Roll</code> method returns the range of roll angles supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum roll angle, in degrees.


### -param pMax [out]

Receives the maximum roll angle, in degrees.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default roll angle, in degrees.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

