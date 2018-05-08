---
UID: NF:vidcap.ICameraControl.put_Exposure
title: ICameraControl::put_Exposure
author: windows-driver-content
description: The put_Exposure method sets the camera's exposure time.
old-location: dshow\icameracontrol_put_exposure.htm
old-project: DirectShow
ms.assetid: 2db9bdb3-c508-40b6-bd5e-75e418ba2f18
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: ICameraControl interface [DirectShow],put_Exposure method, ICameraControl.put_Exposure, ICameraControl::put_Exposure, ICameraControlput_Exposure, dshow.icameracontrol_put_exposure, put_Exposure, put_Exposure method [DirectShow], put_Exposure method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Exposure
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
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	ICameraControl.put_Exposure
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::put_Exposure


## -description


The <code>put_Exposure</code> method sets the camera's exposure time.


## -parameters




### -param Value [in]

Exposure time, in log base 2 seconds. If the value is <i>n</i>, the exposure time is 2^n seconds.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

