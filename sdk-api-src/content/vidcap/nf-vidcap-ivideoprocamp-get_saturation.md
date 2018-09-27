---
UID: NF:vidcap.IVideoProcAmp.get_Saturation
title: IVideoProcAmp::get_Saturation
author: windows-sdk-content
description: The get_Saturation method returns the camera's saturation setting.
old-location: dshow\ivideoprocamp_get_saturation.htm
tech.root: DirectShow
ms.assetid: 977e71a4-8118-4fc2-9f76-ec30293b33d0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Saturation method, IVideoProcAmp.get_Saturation, IVideoProcAmp::get_Saturation, IVideoProcAmpget_Saturation, dshow.ivideoprocamp_get_saturation, get_Saturation, get_Saturation method [DirectShow], get_Saturation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Saturation
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
 - IVideoProcAmp.get_Saturation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_Saturation


## -description


The <code>get_Saturation</code> method returns the camera's saturation setting.


## -parameters




### -param pValue [out]

Receives the saturation setting. Larger values indicate greater saturation. The value zero indicates grayscale.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

