---
UID: NF:vidcap.IVideoProcAmp.put_Hue
title: IVideoProcAmp::put_Hue
author: windows-sdk-content
description: The put_Hue method sets the camera's hue setting.
old-location: dshow\ivideoprocamp_put_hue.htm
old-project: DirectShow
ms.assetid: 7b0926c3-4167-423d-ac5c-ac4df06948aa
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_Hue method, IVideoProcAmp.put_Hue, IVideoProcAmp::put_Hue, IVideoProcAmpput_Hue, dshow.ivideoprocamp_put_hue, put_Hue, put_Hue method [DirectShow], put_Hue method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Hue
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
 - IVideoProcAmp.put_Hue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::put_Hue


## -description


The <code>put_Hue</code> method sets the camera's hue setting.


## -parameters




### -param Value [in]

Specifies the hue setting, in units of degrees * 100. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://msdn.microsoft.com/5625b73c-8033-4930-af26-e7c4b4fb6516">IVideoProcAmp::getRange_Hue</a>.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

