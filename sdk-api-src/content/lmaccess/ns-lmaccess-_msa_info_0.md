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

# _MSA_INFO_0 structure


## -description


Specifies information about a managed service account. This structure is used by the <a href="https://msdn.microsoft.com/ee253cab-bd53-426e-809a-12a1ccdc010b">NetQueryServiceAccount</a> function.


## -struct-fields




### -field State

A value of the <a href="https://msdn.microsoft.com/3cba6c6a-1d63-4795-b009-1fcdf86cc2ef">MSA_INFO_STATE</a> enumeration that indicates the state of the service account specified in the call to the <a href="https://msdn.microsoft.com/ee253cab-bd53-426e-809a-12a1ccdc010b">NetQueryServiceAccount</a> function.

