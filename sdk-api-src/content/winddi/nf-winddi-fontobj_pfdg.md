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

# FONTOBJ_pfdg function


## -description


The <b>FONTOBJ_pfdg</b> function retrieves the pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565625">FD_GLYPHSET</a> structure associated with the specified font.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure for which the associated FD_GLYPHSET structure is to be returned.


## -returns



<b>FONTOBJ_pfdg</b> returns a pointer to the FD_GLYPHSET structure associated with the specified font.




## -remarks



Printer drivers can call <b>FONTOBJ_pfdg</b> to determine which Unicode code points are supported in a GDI font. The printer driver can then determine whether it can optimize performance by instead using a similar printer-resident font to display a text string.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565625">FD_GLYPHSET</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

