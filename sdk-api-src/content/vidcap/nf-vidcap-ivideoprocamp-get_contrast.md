---
UID: NF:vidcap.IVideoProcAmp.get_Contrast
title: IVideoProcAmp::get_Contrast
author: windows-sdk-content
description: The get_Contrast method returns the camera's contrast setting.
old-location: dshow\ivideoprocamp_get_contrast.htm
tech.root: DirectShow
ms.assetid: 04c63013-33f1-42c0-9239-ec012c9a0528
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Contrast method, IVideoProcAmp.get_Contrast, IVideoProcAmp::get_Contrast, IVideoProcAmpget_Contrast, dshow.ivideoprocamp_get_contrast, get_Contrast, get_Contrast method [DirectShow], get_Contrast method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Contrast
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
 - IVideoProcAmp.get_Contrast
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vidcap.h
: 
- IVideoProcAmp.get_Contrast
: 
---

# IVideoProcAmp::get_Contrast


## -description


The <code>get_Contrast</code> method returns the camera's contrast setting.


## -parameters




### -param pValue [out]

Receives the contrast setting. Larger values indicate increased contrast.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

