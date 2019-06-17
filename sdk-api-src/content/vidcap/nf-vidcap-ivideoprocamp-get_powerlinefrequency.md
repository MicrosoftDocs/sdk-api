---
UID: NF:vidcap.IVideoProcAmp.get_PowerlineFrequency
title: IVideoProcAmp::get_PowerlineFrequency (vidcap.h)
author: windows-sdk-content
description: The get_PowerlineFrequency method returns the camera's power line frequency setting. This setting enables the camera to perform anti-flicker processing.
old-location: dshow\ivideoprocamp_get_powerlinefrequency.htm
tech.root: DirectShow
ms.assetid: 8c7bfc4a-895f-45a6-9619-868d1e7bc674
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_PowerlineFrequency method, IVideoProcAmp.get_PowerlineFrequency, IVideoProcAmp::get_PowerlineFrequency, IVideoProcAmpget_PowerlineFrequency, dshow.ivideoprocamp_get_powerlinefrequency, get_PowerlineFrequency, get_PowerlineFrequency method [DirectShow], get_PowerlineFrequency method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_PowerlineFrequency
ms.topic: method
f1_keywords: ["vidcap/IVideoProcAmp.get_PowerlineFrequency"]
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
 - IVideoProcAmp.get_PowerlineFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoProcAmp::get_PowerlineFrequency


## -description


The <code>get_PowerlineFrequency</code> method returns the camera's power line frequency setting. This setting enables the camera to perform anti-flicker processing.


## -parameters




### -param pValue [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
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

Receives one or more flags. See <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagvideoprocampflags">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
 

 

