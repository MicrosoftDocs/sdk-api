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

# _ROOT_INFO_LUID structure


## -description


The <b>ROOT_INFO_LUID</b> structure contains a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>) for Cryptographic Smart Card Root Information. The <a href="https://msdn.microsoft.com/165a1a9e-e426-4823-8d1b-f13c338964c9">CRYPT_SMART_CARD_ROOT_INFO</a> structure includes a <b>ROOT_INFO_LUID</b> structure.


## -struct-fields




### -field LowPart

Low-order bits.


### -field HighPart

High-order bits.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>
 

 

