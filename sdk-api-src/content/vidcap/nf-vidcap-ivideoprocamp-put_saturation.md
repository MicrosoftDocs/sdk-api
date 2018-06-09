---
UID: NF:vidcap.IVideoProcAmp.put_Saturation
title: IVideoProcAmp::put_Saturation
author: windows-sdk-content
description: The put_Saturation method sets the camera's saturation setting.
old-location: dshow\ivideoprocamp_put_saturation.htm
old-project: DirectShow
ms.assetid: 7167fcac-b0c8-444e-a6a9-7ff9a603cc58
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_Saturation method, IVideoProcAmp.put_Saturation, IVideoProcAmp::put_Saturation, IVideoProcAmpput_Saturation, dshow.ivideoprocamp_put_saturation, put_Saturation, put_Saturation method [DirectShow], put_Saturation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Saturation
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
 - IVideoProcAmp.put_Saturation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::put_Saturation


## -description


The <code>put_Saturation</code> method sets the camera's saturation setting.


## -parameters




### -param Value [in]

Specifies the saturation setting. Larger values indicate greater saturation. The value zero indicates grayscale.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

