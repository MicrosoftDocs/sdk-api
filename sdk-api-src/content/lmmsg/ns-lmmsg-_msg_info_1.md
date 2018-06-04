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

# _MSG_INFO_1 structure


## -description


The
				<b>MSG_INFO_1</b> structure specifies a message alias. This structure exists only for compatibility. Message forwarding is not supported.


## -struct-fields




### -field msgi1_name

Pointer to a Unicode string that specifies the alias to which the message is to be sent. The constant LEN specifies the maximum number of characters in the string.


### -field msgi1_forward_flag

This member must be zero.


### -field msgi1_forward

This member must be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/9face737-3472-4a53-97b6-e861a60ee96a">Message Functions</a>



<a href="https://msdn.microsoft.com/fc1b11e6-294d-47d3-8c63-bee80b5a8581">NetMessageNameEnum</a>



<a href="https://msdn.microsoft.com/72129865-2aee-41d5-8a89-53bb815a7f63">NetMessageNameGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

