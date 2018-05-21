---
UID: NF:vidcap.ICameraControl.get_Pan
title: ICameraControl::get_Pan
author: windows-driver-content
description: The get_Pan method returns the camera's panning angle.
old-location: dshow\icameracontrol_get_pan.htm
old-project: DirectShow
ms.assetid: 4cbf7582-63ad-4572-be62-be1fe5bc60b3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICameraControl interface [DirectShow],get_Pan method, ICameraControl.get_Pan, ICameraControl::get_Pan, ICameraControlget_Pan, dshow.icameracontrol_get_pan, get_Pan, get_Pan method [DirectShow], get_Pan method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Pan
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
-	ICameraControl.get_Pan
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_Pan


## -description


The <code>get_Pan</code> method returns the camera's panning angle.


## -parameters




### -param pValue [out]

Receives the panning angle, in degrees. Positive values are clockwise when viewing the camera from above, and negative values are counter clockwise. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://msdn.microsoft.com/390c6330-1eb4-4149-aabc-296b585b577a">ICameraControl::getRange_Pan</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

