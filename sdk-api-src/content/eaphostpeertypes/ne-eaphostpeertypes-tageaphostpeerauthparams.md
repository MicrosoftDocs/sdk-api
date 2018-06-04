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

# tagEapHostPeerAuthParams enumeration


## -description


Defines the set of possible authentication parameter values.


## -enum-fields




### -field EapHostPeerAuthStatus

Contains the current status of authentication for the supplicant.


### -field EapHostPeerIdentity

Contains the user identity of the supplicant.


### -field EapHostPeerIdentityExtendedInfo

Contains extended user identity information for the supplicant from the identity packet.


### -field EapHostNapInfo

Windows 7 or later: Contains NAP-related information for the supplicant in an <a href="https://msdn.microsoft.com/703eda56-5932-44d5-ae7f-0a6328d82237">EapHostPeerNapInfo</a> structure.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014">EAPHost Supplicant Enumerations</a>



<a href="https://msdn.microsoft.com/cb5ceffb-941f-48ad-9271-111f41adc65b">EapHostPeerGetAuthStatus</a>
 

 

