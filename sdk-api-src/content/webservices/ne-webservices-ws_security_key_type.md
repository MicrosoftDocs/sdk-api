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

# WS_SECURITY_KEY_TYPE enumeration


## -description



The key type of a security token.  It is used as the return type when
a security token is queried about its key.  It is also used to specify
the required key type when requesting a security token from a security
token service.
            


## -enum-fields




### -field WS_SECURITY_KEY_TYPE_NONE


Has no key -- it may be a bearer token such as a username/password
pair.
                


### -field WS_SECURITY_KEY_TYPE_SYMMETRIC


Has a symmetric key.
                


### -field WS_SECURITY_KEY_TYPE_ASYMMETRIC


Has an asymmetric key.
                

