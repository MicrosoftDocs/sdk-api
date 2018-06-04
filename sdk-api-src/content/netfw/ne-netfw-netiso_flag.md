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

# NETISO_FLAG enumeration


## -description


The <b>NETISO_FLAG</b> enumerated type specifies whether binaries should be returned for app containers.


## -enum-fields




### -field NETISO_FLAG_FORCE_COMPUTE_BINARIES

Specifies that all binaries will be computed before the app container is returned.

This flag should be set if the caller requires up-to-date and complete information on app container binaries. If this flag is not set, returned data may be stale or incomplete.



### -field NETISO_FLAG_MAX

Maximum value for testing purposes.


## -remarks



By default, binaries are not returned. <b>NETISO_FLAG_FORCE_COMPUTE_BINARIES</b> must be set in order for these to be returned.



