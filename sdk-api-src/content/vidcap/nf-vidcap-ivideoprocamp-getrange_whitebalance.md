---
UID: NF:vidcap.IVideoProcAmp.getRange_WhiteBalance
title: IVideoProcAmp::getRange_WhiteBalance
author: windows-sdk-content
description: The getRange_WhiteBalance method returns the range of white balance settings supported by the camera, expressed as color temperature.
old-location: dshow\ivideoprocamp_getrange_whitebalance.htm
tech.root: DirectShow
ms.assetid: 3c7a21ec-2aa5-4e00-8d7b-a13a366a3f17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_WhiteBalance method, IVideoProcAmp.getRange_WhiteBalance, IVideoProcAmp::getRange_WhiteBalance, IVideoProcAmpgetRange_WhiteBalance, dshow.ivideoprocamp_getrange_whitebalance, getRange_WhiteBalance, getRange_WhiteBalance method [DirectShow], getRange_WhiteBalance method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_WhiteBalance
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
 - IVideoProcAmp.getRange_WhiteBalance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::getRange_WhiteBalance


## -description


The <code>getRange_WhiteBalance</code> method returns the range of white balance settings supported by the camera, expressed as color temperature.


## -parameters




### -param pMin [out]

Receives the minimum white balance, in degrees Kelvin.


### -param pMax [out]

Receives the maximum white balance, in degrees Kelvin.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default white balance.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd407327(v=VS.85).aspx">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377236(v=VS.85).aspx">IVideoProcAmp Interface</a>
 

 

