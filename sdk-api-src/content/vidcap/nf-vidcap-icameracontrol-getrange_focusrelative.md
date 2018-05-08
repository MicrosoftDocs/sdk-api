---
UID: NF:vidcap.ICameraControl.getRange_FocusRelative
title: ICameraControl::getRange_FocusRelative
author: windows-driver-content
description: The getRange_FocusRelative method returns the range of relative focal distances supported by the camera. The relative focus indicates the direction in which the lens group is moving.
old-location: dshow\icameracontrol_getrange_focusrelative.htm
old-project: DirectShow
ms.assetid: c5038a59-bdc4-4034-afd1-256003687187
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_FocusRelative method, ICameraControl.getRange_FocusRelative, ICameraControl::getRange_FocusRelative, ICameraControlgetRange_FocusRelative, dshow.icameracontrol_getrange_focusrelative, getRange_FocusRelative, getRange_FocusRelative method [DirectShow], getRange_FocusRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_FocusRelative
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
-	ICameraControl.getRange_FocusRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::getRange_FocusRelative


## -description


The <code>getRange_FocusRelative</code> method returns the range of relative focal distances supported by the camera. The relative focus indicates the direction in which the lens group is moving.


## -parameters




### -param pMin [out]

Receives the minimum relative focus.


### -param pMax [out]

Receives the minimum relative focus.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default relative focus.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

