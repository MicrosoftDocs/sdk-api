---
UID: NF:vidcap.ICameraControl.get_Tilt
title: ICameraControl::get_Tilt
author: windows-driver-content
description: The get_Tilt method returns the camera's tilt angle.
old-location: dshow\icameracontrol_get_tilt.htm
old-project: DirectShow
ms.assetid: 8e9d9176-fb27-4221-876b-49f407289877
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: ICameraControl interface [DirectShow],get_Tilt method, ICameraControl.get_Tilt, ICameraControl::get_Tilt, ICameraControlget_Tilt, dshow.icameracontrol_get_tilt, get_Tilt, get_Tilt method [DirectShow], get_Tilt method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Tilt
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
-	ICameraControl.get_Tilt
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_Tilt


## -description


The <code>get_Tilt</code> method returns the camera's tilt angle.


## -parameters




### -param pValue [out]

Receives the tilt angle, in degrees. Positive values point the camera up, and negative values point the camera down. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://msdn.microsoft.com/d48920cf-677e-4014-a998-426bb45d1b46">ICameraControl::getRange_Tilt</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

