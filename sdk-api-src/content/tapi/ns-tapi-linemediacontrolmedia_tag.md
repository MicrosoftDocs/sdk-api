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

# linemediacontrolmedia_tag structure


## -description


The 
<b>LINEMEDIACONTROLMEDIA</b> structure describes a media action to be executed when detecting a media type change. It is used as an entry in an array. The 
<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a> and 
<a href="https://msdn.microsoft.com/e9273bd6-8dc3-4b45-bf0e-a1a10d78a604">TSPI_lineSetMediaControl</a> functions use this structure.


## -struct-fields




### -field dwMediaModes

One or more media types. This member uses one of the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ Constants</a>.


### -field dwDuration

Duration of time during which the media type should be present before the application should be notified or media control action should be taken, in milliseconds.


### -field dwMediaControl

Media control action. This member uses one of the 
<a href="https://msdn.microsoft.com/1e8aeda8-2810-462a-bfba-0296d854d9aa">LINEMEDIACONTROL_ Constants</a>.


## -remarks



This structure may not be extended.

The 
<b>LINEMEDIACONTROLMEDIA</b> structure defines a triple &lt;media type(s), duration, media-control action&gt;. An array of these triples is passed to the 
<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a> function to set the media control actions triggered by media type changes for a given call. When a change to a listed media type is detected, then the corresponding action on the media stream is invoked.




## -see-also




<a href="https://msdn.microsoft.com/e9273bd6-8dc3-4b45-bf0e-a1a10d78a604">TSPI_lineSetMediaControl</a>



<a href="https://msdn.microsoft.com/5a4fc83a-6bc9-4081-b374-ddb912fb2242">lineSetMediaControl</a>
 

 

