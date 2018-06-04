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

# tagEapCode enumeration


## -description


 The <b>EapCode</b> enumeration defines the set of EAP packet types.


## -enum-fields




### -field EapCodeMinimum

The lowest possible value for an EAP packet type code. 


### -field EapCodeRequest

A request packet sent by the authenticator to the supplicant.


### -field EapCodeResponse

A response packet sent by the supplicant to the authenticator.


### -field EapCodeSuccess

A successful authentication attempt.


### -field EapCodeFailure

A failed authentication attempt.


### -field EapCodeMaximum

The highest possible value for an EAP packet type code.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/a5d78db0-990f-4318-8f1a-4e903221845f">EapPacket</a>
 

 

