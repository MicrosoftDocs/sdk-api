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

# tagIMECHARPOSITION structure


## -description



Contains information about the character position in the composition window.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwCharPos

Character offset in the composition string, in <b>TCHAR</b> values.


### -field pt

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure containing the coordinate of the top left point of requested character in screen coordinates. The top left point is based on the character baseline in any text flow.


### -field cLineHeight

Height of a line that contains the requested character, in pixels.


### -field rcDocument

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the editable area for text, in screen coordinates, for the application.


## -remarks



When an application uses IME to draw the composition string, the members of this structure are automatically filled. Applications that draw the composition string themselves, rather than relying on the IME, are responsible for filling all the fields defined in the structure.




## -see-also




<a href="https://msdn.microsoft.com/cae7e5b3-8aaf-452d-80df-fb0ae04a342c">IMR_QUERYCHARPOSITION</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

