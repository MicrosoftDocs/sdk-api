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

# tagTLIBATTR structure


## -description


Contains information about a type library. Information from this structure is used to identify the type library and to provide national language support for member names.


## -struct-fields




### -field guid

The globally unique identifier.


### -field lcid

The locale identifier.


### -field syskind

The target hardware platform.


### -field wMajorVerNum

The major version number.


### -field wMinorVerNum

The minor version number.


### -field wLibFlags

The library flags.

