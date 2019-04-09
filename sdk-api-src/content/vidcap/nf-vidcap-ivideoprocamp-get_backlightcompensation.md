---
UID: NF:vidcap.IVideoProcAmp.get_BacklightCompensation
title: IVideoProcAmp::get_BacklightCompensation (vidcap.h)
author: windows-sdk-content
description: The get_BacklightCompensation method returns the camera's backlight compensation setting.
old-location: dshow\ivideoprocamp_get_backlightcompensation.htm
tech.root: DirectShow
ms.assetid: 1b0b4c06-5958-446e-bd06-4ee6f90b6e78
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_BacklightCompensation method, IVideoProcAmp.get_BacklightCompensation, IVideoProcAmp::get_BacklightCompensation, IVideoProcAmpget_BacklightCompensation, dshow.ivideoprocamp_get_backlightcompensation, get_BacklightCompensation, get_BacklightCompensation method [DirectShow], get_BacklightCompensation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_BacklightCompensation
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.get_BacklightCompensation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_BacklightCompensation


## -description


The <code>get_BacklightCompensation</code> method returns the camera's backlight compensation setting.


## -parameters




### -param pValue [out]

Receives the backlight compensation setting. If the value is zero, backlight compensation is disabled. Otherwise, backlight compensation is enabled. The camera may support a Boolean setting (0/1) or a range of settings. If it supports a range of settings, higher numbers indicate a greater degree of backlight compensation.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

