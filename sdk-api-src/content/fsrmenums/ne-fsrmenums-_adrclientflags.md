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

# _AdrClientFlags enumeration


## -description


Enumerates flags for indicating why an access denied remediation (ADR) client operation could not be 
    performed.


## -enum-fields




### -field AdrClientFlags_None

No ADR client flags are specified.


### -field AdrClientFlags_FailForLocalPaths

ADR client operations should fail when local paths are specified.


### -field AdrClientFlags_FailIfNotSupportedByServer

ADR client operations should fail if the operation is not supported by the server.


### -field AdrClientFlags_FailIfNotDomainJoined

ADR client operations should fail if the computer is not joined to a domain.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>
 

 

