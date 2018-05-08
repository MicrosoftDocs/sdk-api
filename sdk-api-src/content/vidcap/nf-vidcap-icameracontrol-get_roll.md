---
UID: NF:vidcap.ICameraControl.get_Roll
title: ICameraControl::get_Roll
author: windows-driver-content
description: "."
old-location: dshow\icameracontrol_get_roll.htm
old-project: DirectShow
ms.assetid: cebe99e1-9bcc-4826-8b15-b4d6757ec5b4
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: ICameraControl interface [DirectShow],get_Roll method, ICameraControl.get_Roll, ICameraControl::get_Roll, ICameraControlget_Roll, dshow.icameracontrol_get_roll, get_Roll, get_Roll method [DirectShow], get_Roll method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Roll
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
-	ICameraControl.get_Roll
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_Roll


## -description




The <code>get_Roll</code> method returns the camera's roll angle.


## -parameters




### -param pValue [out]

Receives the roll angle, in degrees. Positive values are clockwise along the image viewing axis, and negative values are counter clockwise. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://msdn.microsoft.com/14400765-d8a2-4ac2-a26b-39949ecd2bda">ICameraControl::getRange_Roll</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

