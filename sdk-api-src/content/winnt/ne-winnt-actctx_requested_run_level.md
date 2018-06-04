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

# ACTCTX_REQUESTED_RUN_LEVEL enumeration


## -description


The <b>ACTCTX_REQUESTED_RUN_LEVEL</b> enumeration describes the requested run level of the activation context.


## -enum-fields




### -field ACTCTX_RUN_LEVEL_UNSPECIFIED

The application manifest does not specify a requested run level for the application.


### -field ACTCTX_RUN_LEVEL_AS_INVOKER

The application manifest requests the least privilege level to run the application.




### -field ACTCTX_RUN_LEVEL_HIGHEST_AVAILABLE

The application manifest requests the highest privilege level to run the application.


### -field ACTCTX_RUN_LEVEL_REQUIRE_ADMIN

The application manifest requests the administrator privilege level to run the application. 


### -field ACTCTX_RUN_LEVEL_NUMBERS

Total number of possible run levels.

