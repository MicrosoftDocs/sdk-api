---
UID: NF:vidcap.IVideoProcAmp.getRange_Saturation
title: IVideoProcAmp::getRange_Saturation
author: windows-sdk-content
description: The getRange_Saturation method returns the range of saturation settings supported by the camera.
old-location: dshow\ivideoprocamp_getrange_saturation.htm
tech.root: DirectShow
ms.assetid: 7c3d99a4-fc23-4d5e-907e-72272599a684
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_Saturation method, IVideoProcAmp.getRange_Saturation, IVideoProcAmp::getRange_Saturation, IVideoProcAmpgetRange_Saturation, dshow.ivideoprocamp_getrange_saturation, getRange_Saturation, getRange_Saturation method [DirectShow], getRange_Saturation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_Saturation
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
 - IVideoProcAmp.getRange_Saturation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::getRange_Saturation


## -description


The <code>getRange_Saturation</code> method returns the range of saturation settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum saturation setting.


### -param pMax [out]

Receives the maximum saturation setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default saturation setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

