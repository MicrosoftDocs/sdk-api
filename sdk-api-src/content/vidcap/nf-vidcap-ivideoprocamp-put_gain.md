---
UID: NF:vidcap.IVideoProcAmp.put_Gain
title: IVideoProcAmp::put_Gain
author: windows-sdk-content
description: The put_Gain method sets the camera's gain setting.
old-location: dshow\ivideoprocamp_put_gain.htm
tech.root: DirectShow
ms.assetid: 8256c1d9-ca3f-4b6a-921d-a424932927b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_Gain method, IVideoProcAmp.put_Gain, IVideoProcAmp::put_Gain, IVideoProcAmpput_Gain, dshow.ivideoprocamp_put_gain, put_Gain, put_Gain method [DirectShow], put_Gain method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Gain
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
 - IVideoProcAmp.put_Gain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::put_Gain


## -description


The <code>put_Gain</code> method sets the camera's gain setting.


## -parameters




### -param Value [in]

Specifies the gain setting. Larger values indicate higher gain.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

