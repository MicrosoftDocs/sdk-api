---
UID: NF:vidcap.IVideoProcAmp.getRange_WhiteBalanceComponent
title: IVideoProcAmp::getRange_WhiteBalanceComponent
author: windows-sdk-content
description: The getRange_WhiteBalanceComponent method returns the range of white balance settings supported by the camera, expressed as red and blue component values.
old-location: dshow\ivideoprocamp_getrange_whitebalancecomponent.htm
old-project: DirectShow
ms.assetid: dec23c5a-3999-4f9b-81f3-2718b38d5835
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_WhiteBalanceComponent method, IVideoProcAmp.getRange_WhiteBalanceComponent, IVideoProcAmp::getRange_WhiteBalanceComponent, IVideoProcAmpgetRange_WhiteBalanceComponent, dshow.ivideoprocamp_getrange_whitebalancecomponent, getRange_WhiteBalanceComponent, getRange_WhiteBalanceComponent method [DirectShow], getRange_WhiteBalanceComponent method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_WhiteBalanceComponent
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
 - IVideoProcAmp.getRange_WhiteBalanceComponent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::getRange_WhiteBalanceComponent


## -description


The <code>getRange_WhiteBalanceComponent</code> method returns the range of white balance settings supported by the camera, expressed as red and blue component values.


## -parameters




### -param pMin [out]

Receives the minimum white balance.


### -param pMax [out]

Receives the maximum white balance.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default white balance.


### -param pCapsFlag [in, out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

