---
UID: NF:vidcap.IVideoProcAmp.getRange_Gain
title: IVideoProcAmp::getRange_Gain
author: windows-sdk-content
description: The getRange_Gain method returns the range of gain settings supported by the camera.
old-location: dshow\ivideoprocamp_getrange_gain.htm
tech.root: DirectShow
ms.assetid: a039cece-ee44-43e0-ade9-5a7e1d9a1c11
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_Gain method, IVideoProcAmp.getRange_Gain, IVideoProcAmp::getRange_Gain, IVideoProcAmpgetRange_Gain, dshow.ivideoprocamp_getrange_gain, getRange_Gain, getRange_Gain method [DirectShow], getRange_Gain method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_Gain
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
 - IVideoProcAmp.getRange_Gain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::getRange_Gain


## -description


The <code>getRange_Gain</code> method returns the range of gain settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum gain setting.


### -param pMax [out]

Receives the maximum gain setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default gain setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

