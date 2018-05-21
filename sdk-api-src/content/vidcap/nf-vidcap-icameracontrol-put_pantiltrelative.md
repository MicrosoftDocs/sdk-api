---
UID: NF:vidcap.ICameraControl.put_PanTiltRelative
title: ICameraControl::put_PanTiltRelative
author: windows-driver-content
description: The put_PanTiltRelative method sets the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_put_pantiltrelative.htm
old-project: DirectShow
ms.assetid: 69d8303c-2ff2-416d-909c-e9f352e53cf1
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICameraControl interface [DirectShow],put_PanTiltRelative method, ICameraControl.put_PanTiltRelative, ICameraControl::put_PanTiltRelative, ICameraControlput_PanTiltRelative, dshow.icameracontrol_put_pantiltrelative, put_PanTiltRelative, put_PanTiltRelative method [DirectShow], put_PanTiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_PanTiltRelative
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
-	ICameraControl.put_PanTiltRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::put_PanTiltRelative


## -description


The <code>put_PanTiltRelative</code> method sets the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param PanValue [in]

Specifies the relative pan. See <a href="https://msdn.microsoft.com/a4ac28f4-8570-4307-80c1-2960d7c87544">ICameraControl::put_PanRelative</a>.


### -param TiltValue [in]

Specifies the relative tilt. See <a href="https://msdn.microsoft.com/69aa7ecf-4816-460b-b4f8-480c0d4f8331">ICameraControl::put_TiltRelative</a>.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

