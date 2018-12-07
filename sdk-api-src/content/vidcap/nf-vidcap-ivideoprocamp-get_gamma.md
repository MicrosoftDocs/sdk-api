---
UID: NF:vidcap.IVideoProcAmp.get_Gamma
title: IVideoProcAmp::get_Gamma
author: windows-sdk-content
description: The get_Gamma method returns the camera's gamma setting.
old-location: dshow\ivideoprocamp_get_gamma.htm
tech.root: DirectShow
ms.assetid: a8d62862-5509-4401-affe-68dfa96ae60f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Gamma method, IVideoProcAmp.get_Gamma, IVideoProcAmp::get_Gamma, IVideoProcAmpget_Gamma, dshow.ivideoprocamp_get_gamma, get_Gamma, get_Gamma method [DirectShow], get_Gamma method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Gamma
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
 - IVideoProcAmp.get_Gamma
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_Gamma


## -description


The <code>get_Gamma</code> method returns the camera's gamma setting.


## -parameters




### -param pValue [out]

Receives the gamma setting, in units of gamma * 100. Theoretical values range from 1 to 500, but the actual range depends on the camera. See <a href="https://msdn.microsoft.com/36914aed-d11c-42c0-a0e5-ba1d3ba6dd22">IVideoProcAmp::getRange_Gamma</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

