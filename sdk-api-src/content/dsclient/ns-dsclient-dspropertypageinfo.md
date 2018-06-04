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

# DSPROPERTYPAGEINFO structure


## -description


The <b>DSPROPERTYPAGEINFO</b> structure is used by an Active Directory property sheet extension to obtain static registration data for the extension. This structure is  supplied by the <a href="https://msdn.microsoft.com/84ed1322-fee3-44ee-873e-57586261ff62">CFSTR_DSPROPERTYPAGEINFO</a> clipboard format.


## -struct-fields




### -field offsetString

Contains the offset, in bytes, from the start of the <b>DSPROPERTYPAGEINFO</b> structure to a NULL-terminated, Unicode string that contains the optional data stored for the extension.


## -remarks



The  <b>DSPROPETYPAGEINFO</b> structure contains the optional string that the extension added to the <b>adminPropertySheet</b> and/or <b>shellPropertySheet</b> attributes when the extension was registered. For more information about how this string is set, see <a href="https://msdn.microsoft.com/e2d6142b-c2fe-4435-b4af-83f7cd45218b">Registering the Property Page COM Object in a Display Specifier</a>.




## -see-also




<a href="https://msdn.microsoft.com/84ed1322-fee3-44ee-873e-57586261ff62">CFSTR_DSPROPERTYPAGEINFO</a>



<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Display Structures in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/e2d6142b-c2fe-4435-b4af-83f7cd45218b">Registering the Property Page COM Object in a Display Specifier</a>
 

 

