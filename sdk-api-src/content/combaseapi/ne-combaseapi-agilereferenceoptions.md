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

# AgileReferenceOptions enumeration


## -description


Specifies options for the <a href="https://msdn.microsoft.com/D16224C7-1BB7-46F5-B66C-54D0B9679006">RoGetAgileReference</a> function.


## -enum-fields




### -field AGILEREFERENCE_DEFAULT

Use the default marshaling behavior, which is to marshal interfaces when an agile reference to the interface is obtained.


### -field AGILEREFERENCE_DELAYEDMARSHAL

Marshaling happens on demand.  Use this option only in situations where it's known that an object is only resolved from the same apartment in which it was registered.


## -see-also




<a href="https://msdn.microsoft.com/D16224C7-1BB7-46F5-B66C-54D0B9679006">RoGetAgileReference</a>
 

 

