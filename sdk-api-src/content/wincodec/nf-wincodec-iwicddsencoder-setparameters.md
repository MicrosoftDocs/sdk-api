---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWICDdsEncoder::SetParameters


## -description


Sets DDS-specific data.


## -parameters




### -param pParameters [out]

Type: <b><a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>*</b>

Points to the structure where the information is described.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You cannot call this method after you have started to write frame data, for example by calling <a href="https://msdn.microsoft.com/14195781-DA71-400A-B4A7-F336A0B5429B">IWICDdsEncoder::CreateNewFrame</a>.



Setting DDS parameters using this method provides the DDS encoder with information about the expected number of frames and the dimensions and other parameters of each frame. The DDS encoder will fail if you do not set frame data that matches these expectations. For example, if you set <a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters::Width</a> and <b>Height</b> to 32, and <b>MipLevels</b> to 6, the DDS encoder will expect 6 frames with the following dimensions:

<ul>
<li>32x32 pixels.</li>
<li>16x16 pixels.</li>
<li>8x8 pixels.</li>
<li>4x4 pixels.</li>
<li>2x2 pixels.</li>
<li>1x1 pixels.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/DF14309F-7595-4ABE-BB6E-03D2914CC86D">IWICDdsEncoder</a>



<a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>
 

 

