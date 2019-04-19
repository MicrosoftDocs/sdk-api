---
UID: NF:vidcap.ICameraControl.get_PanTilt
title: ICameraControl::get_PanTilt (vidcap.h)
author: windows-sdk-content
description: The get_PanTilt method returns the camera's pan and tilt angles.
old-location: dshow\icameracontrol_get_pantilt.htm
tech.root: DirectShow
ms.assetid: 88f67970-2946-49f9-9c90-e562f37edd83
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_PanTilt method, ICameraControl.get_PanTilt, ICameraControl::get_PanTilt, ICameraControlget_PanTilt, dshow.icameracontrol_get_pantilt, get_PanTilt, get_PanTilt method [DirectShow], get_PanTilt method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PanTilt
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
 - ICameraControl.get_PanTilt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_PanTilt


## -description


The <code>get_PanTilt</code> method returns the camera's pan and tilt angles.


## -parameters




### -param pPanValue [out]

Receives the current panning angle, in arc seconds. An arc second is 1/3600th of a degree. See <a href="https://msdn.microsoft.com/en-us/library/Dd376320(v=VS.85).aspx">ICameraControl::get_Pan</a>.


### -param pTiltValue [out]

Receives the current tilt angle, in arc seconds. See <a href="https://msdn.microsoft.com/en-us/library/Dd376328(v=VS.85).aspx">ICameraControl::get_Tilt</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd318251(v=VS.85).aspx">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376298(v=VS.85).aspx">ICameraControl Interface</a>
 

 

