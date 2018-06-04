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

# RESV_STYLE structure


## -description


The 
<b>RESV_STYLE</b> structure contains information about RSVP RESV style.


## -struct-fields




### -field style_header

RSVP object header, in the form of an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field style_word

RSVP RESV style. Must be one of the following values:

<a id="STYLE_FF"></a>
<a id="style_ff"></a>


#### STYLE_FF

<a id="STYLE_SE"></a>
<a id="style_se"></a>


#### STYLE_SE

<a id="STYLE_WF"></a>
<a id="style_wf"></a>


#### STYLE_WF


## -see-also




<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>
 

 

