---
UID: NF:vidcap.IVideoProcAmp.get_Gamma
title: IVideoProcAmp::get_Gamma (vidcap.h)
author: windows-sdk-content
description: The get_Gamma method returns the camera's gamma setting.
old-location: dshow\ivideoprocamp_get_gamma.htm
tech.root: DirectShow
ms.assetid: a8d62862-5509-4401-affe-68dfa96ae60f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Gamma method, IVideoProcAmp.get_Gamma, IVideoProcAmp::get_Gamma, IVideoProcAmpget_Gamma, dshow.ivideoprocamp_get_gamma, get_Gamma, get_Gamma method [DirectShow], get_Gamma method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Gamma
ms.topic: method
f1_keywords: 
 - "vidcap/IVideoProcAmp.get_Gamma"
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
ms.custom: 19H1
---

# IVideoProcAmp::get_Gamma


## -description


The <code>get_Gamma</code> method returns the camera's gamma setting.


## -parameters




### -param pValue [out]

Receives the gamma setting, in units of gamma * 100. Theoretical values range from 1 to 500, but the actual range depends on the camera. See <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_gamma">IVideoProcAmp::getRange_Gamma</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagvideoprocampflags">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
 

 

