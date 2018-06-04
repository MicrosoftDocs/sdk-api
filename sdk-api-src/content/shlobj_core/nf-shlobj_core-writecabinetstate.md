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

# WriteCabinetState function


## -description


<p class="CCE_Message">[<b>WriteCabinetState</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Writes the information contained in a <a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a> structure into the registry.


## -parameters




### -param pcs [in]

Type: <b><a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4b82b6a8-c4c0-4af2-9612-0551376c1c62">CABINETSTATE</a> structure that holds the values to be set.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>.



