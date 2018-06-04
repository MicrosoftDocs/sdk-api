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

# HSTRING_HEADER structure


## -description


Represents a header for an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>.


## -struct-fields




### -field Reserved


### -field Reserved.Reserved1

<b>Type: <b>PVOID</b>
</b>
Reserved for future use.


### -field Reserved.Reserved2

<b>Type: <b>char[24]</b>
</b>
Reserved for future use in a 64-bit environment.

<b>Type: <b>char[20]</b>
</b>
Reserved for future use in a non 64-bit environment.


## -see-also




<a href="https://msdn.microsoft.com/0361BB7E-DA49-4289-A93E-DE7AAB8712AC">WindowsCreateStringReference</a>
 

 

