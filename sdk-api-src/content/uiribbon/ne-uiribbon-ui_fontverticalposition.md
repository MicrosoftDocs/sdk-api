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

# UI_FONTVERTICALPOSITION enumeration


## -description


Specifies values that identify the vertical-alignment state of a <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a>.


## -enum-fields




### -field UI_FONTVERTICALPOSITION_NOTAVAILABLE

Vertical positioning is not enabled.


### -field UI_FONTVERTICALPOSITION_NOTSET

Vertical positioning is enabled but not toggled.


### -field UI_FONTVERTICALPOSITION_SUPERSCRIPT

Vertical positioning is enabled and toggled for superscript.


### -field UI_FONTVERTICALPOSITION_SUBSCRIPT

Vertical positioning is enabled and toggled for subscript.


## -remarks



<b>UI_FONTVERTICALPOSITION</b> is associated with the <b>Subscript</b> and <b>Superscript</b> toggle buttons of the <i>RichFont</i> <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a> as shown in the following screen shot.

<img alt="Screen shot of the FontControl element with the RichFont attribute set to true." src="images/Markup/FontControl_SubSuper.png"/>
The <b>Subscript</b> and <b>Superscript</b> toggle buttons  are displayed by default in a <a href="https://msdn.microsoft.com/98eddab5-28cb-4b9d-a788-ee28dd6055b1">FontControl</a>, depending on the value of the <i>FontType</i> attribute. 

The <b>Subscript</b> and <b>Superscript</b> buttons are toggled based on the <b>UI_FONTVERTICALPOSITION</b> value in <a href="https://msdn.microsoft.com/a92f845e-b0fc-4e23-9d06-ca16d2becf0b">UI_PKEY_FontProperties_VerticalPositioning</a>.




## -see-also




<a href="https://msdn.microsoft.com/8499a096-aac3-4af3-a4c9-eebf53698744">Constants and Enumerations</a>



<a href="https://msdn.microsoft.com/a92f845e-b0fc-4e23-9d06-ca16d2becf0b">UI_PKEY_FontProperties_VerticalPositioning</a>
 

 

