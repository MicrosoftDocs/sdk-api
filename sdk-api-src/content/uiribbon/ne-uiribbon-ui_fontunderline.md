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

# UI_FONTUNDERLINE enumeration


## -description


Specifies values that identify the underline state of a <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a>.


## -enum-fields




### -field UI_FONTUNDERLINE_NOTAVAILABLE

Underlining is not enabled.


### -field UI_FONTUNDERLINE_NOTSET

Underlining is off.


### -field UI_FONTUNDERLINE_SET

Underlining is on.


## -remarks



<b>UI_FONTUNDERLINE</b> is associated with the <b>Underline</b> toggle button of the <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a> as shown in the following screen shot.

<img alt="Screen shot of the FontControl element with the RichFont attribute set to true." src="images/Markup/FontControl_Underline.png"/>
The <b>Underline</b> toggle button is displayed by default in a <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a> but can be hidden, depending on the value of the <i>FontType</i> attribute.

The <b>Underline</b> button is toggled based on the <b>UI_FONTUNDERLINE</b> value in <a href="https://msdn.microsoft.com/88492558-ab19-4606-8fe0-5f100677b88a">UI_PKEY_FontProperties_Underline</a>.

A solid single line is the only underline style supported by the <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a>.




## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/88492558-ab19-4606-8fe0-5f100677b88a">UI_PKEY_FontProperties_Underline</a>
 

 

