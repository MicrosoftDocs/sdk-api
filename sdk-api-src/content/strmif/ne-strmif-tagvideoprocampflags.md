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

# tagVideoProcAmpFlags enumeration


## -description



The <b>VideoProcAmpFlags</b> enumeration indicates whether a particular video property is controlled manually or automatically.




## -enum-fields




### -field VideoProcAmp_Flags_Auto


            The setting is controlled automatically.
          


### -field VideoProcAmp_Flags_Manual


            The setting is controlled manually.
          


## -remarks



The following flags defined in KsMedia.h are equivalent to the values in <b>VideoProcAmpFlags</b>:

<pre class="syntax" xml:space="preserve"><code>#define KSPROPERTY_VIDEOPROCAMP_FLAGS_AUTO        0X0001L
#define KSPROPERTY_VIDEOPROCAMP_FLAGS_MANUAL      0X0002L</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/28c45790-2e5a-4acb-8a53-93f19c51dc6a">IAMVideoProcAmp Interface</a>
 

 

