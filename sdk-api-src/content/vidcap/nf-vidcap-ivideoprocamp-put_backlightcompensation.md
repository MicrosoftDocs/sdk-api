---
UID: NF:vidcap.IVideoProcAmp.put_BacklightCompensation
title: IVideoProcAmp::put_BacklightCompensation
author: windows-sdk-content
description: The put_BacklightCompensation method sets the camera's backlight compensation.
old-location: dshow\ivideoprocamp_put_backlightcompensation.htm
old-project: DirectShow
ms.assetid: 52a9a841-b3d0-41fe-b531-70fa6bac4517
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_BacklightCompensation method, IVideoProcAmp.put_BacklightCompensation, IVideoProcAmp::put_BacklightCompensation, IVideoProcAmpput_BacklightCompensation, dshow.ivideoprocamp_put_backlightcompensation, put_BacklightCompensation, put_BacklightCompensation method [DirectShow], put_BacklightCompensation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_BacklightCompensation
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.put_BacklightCompensation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::put_BacklightCompensation


## -description


The <code>put_BacklightCompensation</code> method sets the camera's backlight compensation.


## -parameters




### -param Value [in]

Specifies the backlight compensation setting. If the value is zero, backlight compensation is disabled. Otherwise, backlight compensation is enabled. The camera may support a Boolean setting (0/1) or a range of settings. If it supports a range of settings, higher numbers indicate a greater degree of backlight compensation.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

