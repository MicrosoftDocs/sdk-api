---
UID: NF:vidcap.IVideoProcAmp.getRange_BacklightCompensation
title: IVideoProcAmp::getRange_BacklightCompensation
author: windows-driver-content
description: The getRange_BacklightCompensation method returns the range of backlight compensation settings supported by the camera.
old-location: dshow\ivideoprocamp_getrange_backlightcompensation.htm
old-project: DirectShow
ms.assetid: 4527e7e9-372c-4883-a068-1ce53eb2256a
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_BacklightCompensation method, IVideoProcAmp.getRange_BacklightCompensation, IVideoProcAmp::getRange_BacklightCompensation, IVideoProcAmpgetRange_BacklightCompensation, dshow.ivideoprocamp_getrange_backlightcompensation, getRange_BacklightCompensation, getRange_BacklightCompensation method [DirectShow], getRange_BacklightCompensation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_BacklightCompensation
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
-	IVideoProcAmp.getRange_BacklightCompensation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::getRange_BacklightCompensation


## -description


The <code>getRange_BacklightCompensation</code> method returns the range of backlight compensation settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum backlight compensation setting.


### -param pMax [out]

Receives the maximum backlight compensation setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default backlight compensation setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

