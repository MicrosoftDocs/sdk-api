---
UID: NF:vidcap.IVideoProcAmp.getRange_DigitalMultiplier
title: IVideoProcAmp::getRange_DigitalMultiplier method
author: windows-driver-content
description: The getRange_DigitalMultiplier method returns the range of digital zoom levels supported by the camera.
old-location: dshow\ivideoprocamp_getrange_digitalmultiplier.htm
old-project: DirectShow
ms.assetid: 8a8a5f72-d51f-4f5a-95e4-ac8d1ac1b24f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IVideoProcAmp, IVideoProcAmp interface [DirectShow], getRange_DigitalMultiplier method, IVideoProcAmp::getRange_DigitalMultiplier, IVideoProcAmpgetRange_DigitalMultiplier, dshow.ivideoprocamp_getrange_digitalmultiplier, getRange_DigitalMultiplier method [DirectShow], getRange_DigitalMultiplier method [DirectShow], IVideoProcAmp interface, getRange_DigitalMultiplier,IVideoProcAmp.getRange_DigitalMultiplier, vidcap/IVideoProcAmp::getRange_DigitalMultiplier
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
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vidcap.h
api_name:
-	IVideoProcAmp.getRange_DigitalMultiplier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::getRange_DigitalMultiplier method


## -description


The <code>getRange_DigitalMultiplier</code> method returns the range of digital zoom levels supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum digital zoom level.


### -param pMax [out]

Receives the maximum digital zoom level.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default digital zoom level.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

