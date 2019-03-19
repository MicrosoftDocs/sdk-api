---
UID: NF:vidcap.ICameraControl.getRange_Pan
title: ICameraControl::getRange_Pan (vidcap.h)
author: windows-sdk-content
description: The getRange_Pan method returns the range of panning angles supported by the camera.
old-location: dshow\icameracontrol_getrange_pan.htm
tech.root: DirectShow
ms.assetid: 390c6330-1eb4-4149-aabc-296b585b577a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICameraControl interface [DirectShow],getRange_Pan method, ICameraControl.getRange_Pan, ICameraControl::getRange_Pan, ICameraControlgetRange_Pan, dshow.icameracontrol_getrange_pan, getRange_Pan, getRange_Pan method [DirectShow], getRange_Pan method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_Pan
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
 - ICameraControl.getRange_Pan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::getRange_Pan


## -description


The <code>getRange_Pan</code> method returns the range of panning angles supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum panning angle, in units of 1 arc second.


### -param pMax [out]

Receives the maximum panning angle, in units of 1 arc second.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default panning angle.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd318251(v=VS.85).aspx">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376298(v=VS.85).aspx">ICameraControl Interface</a>
 

 

