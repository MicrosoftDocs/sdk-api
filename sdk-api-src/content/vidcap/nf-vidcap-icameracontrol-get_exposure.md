---
UID: NF:vidcap.ICameraControl.get_Exposure
title: ICameraControl::get_Exposure
author: windows-sdk-content
description: The get_Exposure method returns the camera's exposure time.
old-location: dshow\icameracontrol_get_exposure.htm
old-project: DirectShow
ms.assetid: 19323477-8dc7-46ed-b6a3-d0dd8b103924
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ICameraControl interface [DirectShow],get_Exposure method, ICameraControl.get_Exposure, ICameraControl::get_Exposure, ICameraControlget_Exposure, dshow.icameracontrol_get_exposure, get_Exposure, get_Exposure method [DirectShow], get_Exposure method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Exposure
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
 - ICameraControl.get_Exposure
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_Exposure


## -description


The <code>get_Exposure</code> method returns the camera's exposure time.


## -parameters




### -param pValue [out]

Receives the exposure time, in log base 2 seconds. If the value is <i>n</i>, the exposure time is 2^n seconds.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

