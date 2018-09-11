---
UID: NF:vidcap.IVideoProcAmp.get_ColorEnable
title: IVideoProcAmp::get_ColorEnable
author: windows-sdk-content
description: The get_ColorEnable method returns the camera's color-enable setting.
old-location: dshow\ivideoprocamp_get_colorenable.htm
tech.root: DirectShow
ms.assetid: 6097b8cf-b46e-443d-8f32-46eb4a8f4de6
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_ColorEnable method, IVideoProcAmp.get_ColorEnable, IVideoProcAmp::get_ColorEnable, IVideoProcAmpget_ColorEnable, dshow.ivideoprocamp_get_colorenable, get_ColorEnable, get_ColorEnable method [DirectShow], get_ColorEnable method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_ColorEnable
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
 - IVideoProcAmp.get_ColorEnable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::get_ColorEnable


## -description


The <code>get_ColorEnable</code> method returns the camera's color-enable setting.


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
<td>Color disabled.</td>
</tr>
<tr>
<td>1</td>
<td>Color enabled.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

