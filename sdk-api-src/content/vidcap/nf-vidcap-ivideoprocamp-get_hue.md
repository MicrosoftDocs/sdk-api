---
UID: NF:vidcap.IVideoProcAmp.get_Hue
title: IVideoProcAmp::get_Hue
author: windows-sdk-content
description: The get_Hue method returns the camera's hue setting.
old-location: dshow\ivideoprocamp_get_hue.htm
tech.root: DirectShow
ms.assetid: dfdd44b5-fd39-40da-95b8-9008aef10f9a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Hue method, IVideoProcAmp.get_Hue, IVideoProcAmp::get_Hue, IVideoProcAmpget_Hue, dshow.ivideoprocamp_get_hue, get_Hue, get_Hue method [DirectShow], get_Hue method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Hue
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
 - IVideoProcAmp.get_Hue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_Hue


## -description


The <code>get_Hue</code> method returns the camera's hue setting.


## -parameters




### -param pValue [out]

Receives the hue setting, in units of degrees * 100. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="https://msdn.microsoft.com/5625b73c-8033-4930-af26-e7c4b4fb6516">IVideoProcAmp::getRange_Hue</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

