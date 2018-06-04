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

# WS_PROTECTION_LEVEL enumeration


## -description



Defines the required integrity and confidentiality levels for sent and
received messages.  With transport and mixed-mode security bindings,
this setting applies to each message as a whole.  With message
security, the protection level is specified at the granularity of a
message header or body.  The default value defined applies only to
transport and mixed-mode security.
            


## -enum-fields




### -field WS_PROTECTION_LEVEL_NONE


No signing or encryption.
                


### -field WS_PROTECTION_LEVEL_SIGN


Only signing.
                


### -field WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT


Signing and encryption.
                

