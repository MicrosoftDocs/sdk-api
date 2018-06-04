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

# _AdrEmailFlags enumeration


## -description


Describes the options for access denied remediation (ADR) email.


## -enum-fields




### -field AdrEmailFlags_PutDataOwnerOnToLine

The ADR email will include the owner on the To: line.


### -field AdrEmailFlags_PutAdminOnToLine

The ADR email will include the administrator on the To: line.


### -field AdrEmailFlags_IncludeDeviceClaims

The ADR email will include the device claims.


### -field AdrEmailFlags_IncludeUserInfo

The ADR email will include the user information.


### -field AdrEmailFlags_GenerateEventLog

When the ADR email is sent, an entry will be added to the event log.


## -see-also




<a href="https://msdn.microsoft.com/93fdf667-8959-40a9-a374-c54ed73bbe89">FSRM Enumerations</a>
 

 

