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

# IPSEC_TOKEN0_ structure


## -description


The <b>IPSEC_TOKEN0</b> structure contains various information about an IPsec-specific access token.


## -struct-fields




### -field type

An <a href="https://msdn.microsoft.com/68eb9301-33d9-4ab9-b3e7-0fc83b6f0f1d">IPSEC_TOKEN_TYPE</a> value that specifies the type of token.


### -field principal

An <a href="https://msdn.microsoft.com/f61944aa-2545-4fdd-8bae-6271d4535acc">IPSEC_TOKEN_PRINCIPAL</a> value that specifies the token principal.


### -field mode

An <a href="https://msdn.microsoft.com/5f90e473-39e1-4eed-9ea1-1f20929d5a07">IPSEC_TOKEN_MODE</a> value that indicates in which mode the token was obtained.


### -field token

Handle to the access token.  An <b>IPSEC_TOKEN_HANDLE</b> is of type <b>UINT64</b>.


## -remarks



<b>IPSEC_TOKEN0</b> is a specific implementation of IPSEC_TOKEN. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.



