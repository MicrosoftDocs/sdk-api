---
UID: NF:vidcap.IVideoProcAmp.getRange_Sharpness
title: IVideoProcAmp::getRange_Sharpness
author: windows-sdk-content
description: The getRange_Sharpness method returns the range of sharpness settings supported by the camera.
old-location: dshow\ivideoprocamp_getrange_sharpness.htm
old-project: DirectShow
ms.assetid: 9a5fe298-e76b-44ac-9fcd-a5d1aeb3593c
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_Sharpness method, IVideoProcAmp.getRange_Sharpness, IVideoProcAmp::getRange_Sharpness, IVideoProcAmpgetRange_Sharpness, dshow.ivideoprocamp_getrange_sharpness, getRange_Sharpness, getRange_Sharpness method [DirectShow], getRange_Sharpness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_Sharpness
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
 - IVideoProcAmp.getRange_Sharpness
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::getRange_Sharpness


## -description


The <code>getRange_Sharpness</code> method returns the range of sharpness settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum sharpness setting.


### -param pMax [out]

Receives the maximum sharpness setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default sharpness setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

