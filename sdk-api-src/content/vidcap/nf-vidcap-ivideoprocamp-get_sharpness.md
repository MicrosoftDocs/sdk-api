---
UID: NF:vidcap.IVideoProcAmp.get_Sharpness
title: IVideoProcAmp::get_Sharpness
author: windows-sdk-content
description: The get_Sharpness method returns the camera's sharpness setting.
old-location: dshow\ivideoprocamp_get_sharpness.htm
tech.root: DirectShow
ms.assetid: 12cb9934-4cef-4356-9b59-6b4e6caca573
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Sharpness method, IVideoProcAmp.get_Sharpness, IVideoProcAmp::get_Sharpness, IVideoProcAmpget_Sharpness, dshow.ivideoprocamp_get_sharpness, get_Sharpness, get_Sharpness method [DirectShow], get_Sharpness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Sharpness
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
 - IVideoProcAmp.get_Sharpness
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_Sharpness


## -description


The <code>get_Sharpness</code> method returns the camera's sharpness setting.


## -parameters




### -param pValue [out]

Receives the sharpness setting. Larger values indicate increasing sharpness.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

