---
UID: NF:vidcap.ICameraControl.getRange_RollRelative
title: ICameraControl::getRange_RollRelative
author: windows-sdk-content
description: The getRange_RollRelative method returns the range of relative roll angles supported by the camera. The relative roll is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_getrange_rollrelative.htm
old-project: DirectShow
ms.assetid: c0208111-8648-4511-99f6-20489a026c91
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_RollRelative method, ICameraControl.getRange_RollRelative, ICameraControl::getRange_RollRelative, ICameraControlgetRange_RollRelative, dshow.icameracontrol_getrange_rollrelative, getRange_RollRelative, getRange_RollRelative method [DirectShow], getRange_RollRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_RollRelative
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
 - ICameraControl.getRange_RollRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::getRange_RollRelative


## -description


The <code>getRange_RollRelative</code> method returns the range of relative roll angles supported by the camera. The relative roll is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pMin [out]

Receives the minimum relative roll angle.


### -param pMax [out]

Receives the maximum relative roll angle.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default relative roll angle.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

