---
UID: NF:vidcap.IVideoProcAmp.getRange_DigitalMultiplier
title: IVideoProcAmp::getRange_DigitalMultiplier
author: windows-sdk-content
description: The getRange_DigitalMultiplier method returns the range of digital zoom levels supported by the camera.
old-location: dshow\ivideoprocamp_getrange_digitalmultiplier.htm
tech.root: DirectShow
ms.assetid: 8a8a5f72-d51f-4f5a-95e4-ac8d1ac1b24f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_DigitalMultiplier method, IVideoProcAmp.getRange_DigitalMultiplier, IVideoProcAmp::getRange_DigitalMultiplier, IVideoProcAmpgetRange_DigitalMultiplier, dshow.ivideoprocamp_getrange_digitalmultiplier, getRange_DigitalMultiplier, getRange_DigitalMultiplier method [DirectShow], getRange_DigitalMultiplier method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_DigitalMultiplier
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
 - IVideoProcAmp.getRange_DigitalMultiplier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::getRange_DigitalMultiplier


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

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

