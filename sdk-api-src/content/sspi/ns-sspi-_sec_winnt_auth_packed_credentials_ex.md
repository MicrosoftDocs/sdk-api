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

# _SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX structure


## -description


Specifies serialized credentials and a list of security packages that support the credentials.


## -struct-fields




### -field cbHeaderLength

The size, in bytes, of the structure header.


### -field Flags

This member is reserved. Do not use it.


### -field PackedCredentials

The offset and size of the serialized credentials in this structure.


### -field PackageList

The offset and size of the list of security packages in this structure.

