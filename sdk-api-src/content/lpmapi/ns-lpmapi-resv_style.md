---
UID: NS:lpmapi.RESV_STYLE
title: RESV_STYLE
author: windows-sdk-content
description: The RESV_STYLE structure contains information about RSVP RESV style.
old-location: qos\resv_style.htm
tech.root: QOS
ms.assetid: facc4217-1e6f-44af-bc04-84993f2dfeec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RESV_STYLE, RESV_STYLE structure [QOS], STYLE_FF, STYLE_SE, STYLE_WF, lpmapi/RESV_STYLE, qos.resv_style
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Lpmapi.h
api_name:
 - RESV_STYLE
product: Windows
targetos: Windows
req.typenames: RESV_STYLE
req.redist: 
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
 

 

