---
UID: NE:strmif.tagVideoProcAmpFlags
title: tagVideoProcAmpFlags
author: windows-sdk-content
description: The VideoProcAmpFlags enumeration indicates whether a particular video property is controlled manually or automatically.
old-location: dshow\videoprocampflags.htm
tech.root: DirectShow
ms.assetid: 42876f3b-d2b9-4ddb-85c0-80f5177eef6b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: VideoProcAmpFlags, VideoProcAmpFlags enumeration [DirectShow], VideoProcAmpFlagsEnumeration, VideoProcAmp_Flags_Auto, VideoProcAmp_Flags_Manual, dshow.videoprocampflags, strmif/VideoProcAmpFlags, strmif/VideoProcAmp_Flags_Auto, strmif/VideoProcAmp_Flags_Manual, tagVideoProcAmpFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VideoProcAmpFlags
product: Windows
targetos: Windows
req.typenames: VideoProcAmpFlags
req.redist: 
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
 

 

