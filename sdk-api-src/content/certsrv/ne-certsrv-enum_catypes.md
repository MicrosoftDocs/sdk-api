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

# ENUM_CATYPES enumeration


## -description


The <b>ENUM_CATYPES</b> enumeration specifies a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) type.


## -enum-fields




### -field ENUM_ENTERPRISE_ROOTCA

A root CA that is a member of an Active Directory domain and uses Directory Service to issue and manage certificates.


### -field ENUM_ENTERPRISE_SUBCA

A CA  that uses Directory Service to issue and manage certificates and is subordinate to an enterprise root CA.


### -field ENUM_STANDALONE_ROOTCA

A root CA that does not use Directory Service to issue or manage certificates. It might or might not belong to a domain.


### -field ENUM_STANDALONE_SUBCA

A CA that does not use Directory Service to issue or manage certificates and is subordinate to a standalone root CA.


### -field ENUM_UNKNOWN_CA

An unknown CA type.

