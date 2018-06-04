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

# phoneextensionid_tag structure


## -description


The 
<b>PHONEEXTENSIONID</b> structure describes an extension identifier. Extension identifiers are used to identify service provider-specific extensions for phone device classes. The 
<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a> and 
<a href="https://msdn.microsoft.com/c4c1c68f-0a48-40f2-8eb9-f54c3572578c">TSPI_phoneGetExtensionID</a> functions return this structure.


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



These four members together specify a universally unique extension identifier that identifies a phone device class extension. This structure may not be extended.

Extension identifiers are generated using an SDK-provided generation utility.




## -see-also




<a href="https://msdn.microsoft.com/c4c1c68f-0a48-40f2-8eb9-f54c3572578c">TSPI_phoneGetExtensionID</a>



<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a>
 

 

