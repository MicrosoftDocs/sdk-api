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

# lineextensionid_tag structure


## -description


The 
<b>LINEEXTENSIONID</b> structure describes an extension identifier. Extension identifiers are used to identify service provider-specific extensions for line devices. Multiple functions use this structure, including the 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> function and the 
<a href="https://msdn.microsoft.com/aaea0a6a-bf22-491f-b1bf-d2195fba6af5">TSPI_lineGetExtensionID</a> function.


## -struct-fields




### -field dwExtensionID0

First part of the extension identifier.


### -field dwExtensionID1

Second part of the extension identifier.


### -field dwExtensionID2

Third part of the extension identifier.


### -field dwExtensionID3

Fourth part of the extension identifier.


## -remarks



These four members together specify a universally unique extension identifier that identifies a line device class extension. This structure may not be extended.

Extension identifiers are generated using an SDK-provided generation utility.




## -see-also




<a href="https://msdn.microsoft.com/aaea0a6a-bf22-491f-b1bf-d2195fba6af5">TSPI_lineGetExtensionID</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>
 

 

