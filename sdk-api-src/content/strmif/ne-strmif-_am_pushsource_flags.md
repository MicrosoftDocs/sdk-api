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

# _AM_PUSHSOURCE_FLAGS enumeration


## -description



Indicates the behavior of a live source filter.




## -enum-fields




### -field AM_PUSHSOURCECAPS_INTERNAL_RM


            The filter uses its own rate-matching mechanism; the renderer should therefore not attempt to match rates with this filter.
          


### -field AM_PUSHSOURCECAPS_NOT_LIVE


            The filter is not live. Do not treat it as a live source, even though it exposes the <a href="https://msdn.microsoft.com/5ab294a8-f250-405c-a589-68998bc04cdf">IAMPushSource</a> interface.
          


### -field AM_PUSHSOURCECAPS_PRIVATE_CLOCK


            The filter time stamps the samples using a private clock. The clock is not available to the rest of the graph through <a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock</a>.
          


### -field AM_PUSHSOURCEREQS_USE_STREAM_CLOCK


            Reserved; do not use.
          


### -field AM_PUSHSOURCEREQS_USE_CLOCK_CHAIN




## -remarks



If no flags are set (the default case), the source filter is assumed to be live and not to perform any rate matching on its own.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

