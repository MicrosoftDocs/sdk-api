---
UID: NF:vidcap.IVideoProcAmp.get_PowerlineFrequency
title: IVideoProcAmp::get_PowerlineFrequency
author: windows-sdk-content
description: The get_PowerlineFrequency method returns the camera's power line frequency setting. This setting enables the camera to perform anti-flicker processing.
old-location: dshow\ivideoprocamp_get_powerlinefrequency.htm
old-project: DirectShow
ms.assetid: 8c7bfc4a-895f-45a6-9619-868d1e7bc674
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_PowerlineFrequency method, IVideoProcAmp.get_PowerlineFrequency, IVideoProcAmp::get_PowerlineFrequency, IVideoProcAmpget_PowerlineFrequency, dshow.ivideoprocamp_get_powerlinefrequency, get_PowerlineFrequency, get_PowerlineFrequency method [DirectShow], get_PowerlineFrequency method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_PowerlineFrequency
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
 - IVideoProcAmp.get_PowerlineFrequency
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::get_PowerlineFrequency


## -description


The <code>get_PowerlineFrequency</code> method returns the camera's power line frequency setting. This setting enables the camera to perform anti-flicker processing.


## -parameters




### -param pValue [out]

Receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Disabled.</td>
</tr>
<tr>
<td>1</td>
<td>50 Hz.</td>
</tr>
<tr>
<td>2</td>
<td>60 Hz.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

