---
UID: NF:vidcap.ICameraControl.put_Pan
title: ICameraControl::put_Pan
author: windows-sdk-content
description: The put_Pan method sets the camera's panning angle.
old-location: dshow\icameracontrol_put_pan.htm
tech.root: DirectShow
ms.assetid: 71dc3fe3-089c-46e8-a63b-7a638068d069
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICameraControl interface [DirectShow],put_Pan method, ICameraControl.put_Pan, ICameraControl::put_Pan, ICameraControlput_Pan, dshow.icameracontrol_put_pan, put_Pan, put_Pan method [DirectShow], put_Pan method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Pan
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
 - ICameraControl.put_Pan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::put_Pan


## -description


The <code>put_Pan</code> method sets the camera's panning angle.


## -parameters




### -param Value [in]

Specifies the panning angle, in degrees. Positive values are clockwise when viewing the camera from above, and negative values are counter clockwise. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://msdn.microsoft.com/en-us/library/Dd376305(v=VS.85).aspx">ICameraControl::getRange_Pan</a>.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd318251(v=VS.85).aspx">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376298(v=VS.85).aspx">ICameraControl Interface</a>
 

 

