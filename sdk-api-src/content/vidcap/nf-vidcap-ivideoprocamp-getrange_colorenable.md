---
UID: NF:vidcap.IVideoProcAmp.getRange_ColorEnable
title: IVideoProcAmp::getRange_ColorEnable
author: windows-sdk-content
description: The getRange_ColorEnable method returns the range of color-enable settings supported by the camera.
old-location: dshow\ivideoprocamp_getrange_colorenable.htm
tech.root: DirectShow
ms.assetid: d9041f2a-cf38-419b-be8f-a55599b9a1d9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_ColorEnable method, IVideoProcAmp.getRange_ColorEnable, IVideoProcAmp::getRange_ColorEnable, IVideoProcAmpgetRange_ColorEnable, dshow.ivideoprocamp_getrange_colorenable, getRange_ColorEnable, getRange_ColorEnable method [DirectShow], getRange_ColorEnable method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_ColorEnable
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVideoProcAmp.getRange_ColorEnable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::getRange_ColorEnable


## -description


The <code>getRange_ColorEnable</code> method returns the range of color-enable settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum color-enable setting.


### -param pMax [out]

Receives the maximum color-enable setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default color-enable setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

