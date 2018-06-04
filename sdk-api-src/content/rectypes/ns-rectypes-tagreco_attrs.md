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

# tagRECO_ATTRS structure


## -description



Retrieves the attributes of a recognizer or specifies which attributes to use when you search for an installed recognizer.




## -struct-fields




### -field dwRecoCapabilityFlags


### -field awcVendorName

Vendor who wrote the recognizer.


### -field awcFriendlyName

A human-readable name for the recognizer.

Specify this name when you search for an installed recognizer.


### -field awLanguageId

List of language and sublanguage combinations that the recognizer supports. The list is <b>NULL</b> -terminated.

Specify language identifiers when you search for an installed recognizer if the <i>awcFriendlyName</i> member contains an empty string. Use the MAKELANGID macro to create the language identifiers. If the recognizer does not distinguish between writing styles corresponding to different sublanguages, specify SUBLANG_NEUTRAL for the sublanguage identifier.


## -remarks



The <i>awcFriendlyName</i> parameter may be empty (that is, having the first element set to the null character) when you use this structure as a return value from the <a href="https://msdn.microsoft.com/45683203-1886-4542-8b66-84861862cb6a">GetRecoAttributes Function</a>. Because this is not an error, the return code for <i>awcFriendlyName</i> in <b>GetRecoAttributes Function</b> will be S_OK, and the other fields will contain data.




## -see-also




<a href="https://msdn.microsoft.com/45683203-1886-4542-8b66-84861862cb6a">GetRecoAttributes Function</a>
 

 

