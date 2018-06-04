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

# AUTHZ_SID_OPERATION enumeration


## -description


The <b>AUTHZ_SID_OPERATION</b> enumeration indicates the type of SID operations that can be made by a call to the <a href="https://msdn.microsoft.com/740569A5-6159-409B-B8CB-B3A8BAE4F398">AuthzModifySids</a> function.


## -enum-fields




### -field AUTHZ_SID_OPERATION_NONE

Do not modify anything.


### -field AUTHZ_SID_OPERATION_REPLACE_ALL

Deletes all existing SIDs and replaces them with the specified SIDs. If the replacement SIDs are not specified, all existing SIDs are deleted. This operation can be specified only once and must be the only operation specified.


### -field AUTHZ_SID_OPERATION_ADD

Adds a new SID. If the SID already exists, the call fails.


### -field AUTHZ_SID_OPERATION_DELETE

Deletes the specified SID. If no matching SID is found, no modifications are done and the call fails.


### -field AUTHZ_SID_OPERATION_REPLACE

Replaces the existing SID with the specified SID. If the SID does not already exist, then adds the SID.

