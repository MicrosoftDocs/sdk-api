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

# _formatrange structure


## -description


Information that a rich edit control uses to format its output for a particular device. This structure is used with the <a href="https://msdn.microsoft.com/6d1e562b-d741-4d4a-a395-554083cb0dbb">EM_FORMATRANGE</a> message.


## -struct-fields




### -field hdcTarget

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

An HDC for the target device to format for. 


### -field hdc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

A HDC for the device to render to, if <a href="https://msdn.microsoft.com/6d1e562b-d741-4d4a-a395-554083cb0dbb">EM_FORMATRANGE</a> is being used to send the output to a device.


### -field rc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The area within the <i>rcPage</i> rectangle to render to. Units are measured in twips. 


### -field rcPage

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The entire area of a page on the rendering device. Units are measured in twips. 


### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The range of characters to format.


## -remarks



<b>hdcTarget</b> contains the HDC to format for, which is usually the same as the HDC specified by <b>hdc</b> but can be different. For example, if you create a print preview module, <b>hdc</b> is the HDC of the window in which the output is viewed, and <b>hdcTarget</b> is the HDC for the printer. 
	

The values for <b>rc</b> and <b>rcPage</b> can be obtained by using <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>. 




## -see-also




<a href="https://msdn.microsoft.com/6d1e562b-d741-4d4a-a395-554083cb0dbb">EM_FORMATRANGE</a>
 

 

