---
UID: NF:vidcap.IVideoProcAmp.put_ColorEnable
title: IVideoProcAmp::put_ColorEnable
author: windows-sdk-content
description: The put_ColorEnable method sets the camera's color-enable setting.
old-location: dshow\ivideoprocamp_put_colorenable.htm
tech.root: DirectShow
ms.assetid: 6a1caa3f-e591-4176-90b9-80a4bd71533b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_ColorEnable method, IVideoProcAmp.put_ColorEnable, IVideoProcAmp::put_ColorEnable, IVideoProcAmpput_ColorEnable, dshow.ivideoprocamp_put_colorenable, put_ColorEnable, put_ColorEnable method [DirectShow], put_ColorEnable method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_ColorEnable
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
 - IVideoProcAmp.put_ColorEnable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoProcAmp::put_ColorEnable


## -description


The <code>put_ColorEnable</code> method sets the camera's color-enable setting.


## -parameters




### -param Value [in]

Specifies one of the following values.

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
 


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

