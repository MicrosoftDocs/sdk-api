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

# WS_SECURITY_KEY_ENTROPY_MODE enumeration


## -description



Defines how randomness should be contributed to the issued key during
a security token negotiation done with message and mixed-mode security.
            


## -enum-fields




### -field WS_SECURITY_KEY_ENTROPY_MODE_CLIENT_ONLY


Only client contributes entropy.
                


### -field WS_SECURITY_KEY_ENTROPY_MODE_SERVER_ONLY


Only service contributes entropy.
                


### -field WS_SECURITY_KEY_ENTROPY_MODE_COMBINED


Both contribute entropy.
                

