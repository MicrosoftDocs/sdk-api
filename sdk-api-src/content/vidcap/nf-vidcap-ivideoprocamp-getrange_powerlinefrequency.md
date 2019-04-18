---
UID: NF:vidcap.IVideoProcAmp.getRange_PowerlineFrequency
title: IVideoProcAmp::getRange_PowerlineFrequency (vidcap.h)
author: windows-sdk-content
description: The getRange_PowerlineFrequency method returns the range of power line frequency settings supported by the camera.
old-location: dshow\ivideoprocamp_getrange_powerlinefrequency.htm
tech.root: DirectShow
ms.assetid: f6bb1df3-d033-4627-b5ea-574a2ebf43aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_PowerlineFrequency method, IVideoProcAmp.getRange_PowerlineFrequency, IVideoProcAmp::getRange_PowerlineFrequency, IVideoProcAmpgetRange_PowerlineFrequency, dshow.ivideoprocamp_getrange_powerlinefrequency, getRange_PowerlineFrequency, getRange_PowerlineFrequency method [DirectShow], getRange_PowerlineFrequency method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_PowerlineFrequency
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
 - IVideoProcAmp.getRange_PowerlineFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoProcAmp::getRange_PowerlineFrequency


## -description


The <code>getRange_PowerlineFrequency</code> method returns the range of power line frequency settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum power line frequency setting.


### -param pMax [out]

Receives the maximum power line frequency setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default power line frequency setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

