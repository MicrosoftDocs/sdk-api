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

# CreationProperties function


## -description


Returns a  <a href="https://msdn.microsoft.com/657439fe-dc17-42af-9e2c-2f3cb769a5a3">D2D1_CREATION_PROPERTIES</a> that describes root-level creation details.


## -parameters




### -param threadingMode

Type: <b><a href="https://msdn.microsoft.com/21fba5ee-3d31-4142-b66a-94b343e1c6eb">D2D1_THREADING_MODE</a></b>

The threading mode with which the corresponding root objects are created.


### -param debugLevel

Type: <b><a href="https://msdn.microsoft.com/3f1b4127-12d4-4472-ae26-0b69fdbb35a7">D2D1_DEBUG_LEVEL</a></b>

The debug level that the root objects should be created with.


### -param options

Type: <b><a href="https://msdn.microsoft.com/be4e6eb7-0767-4faf-9f27-eeb3bed48244">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The device context options that the root objects should be created with.


## -returns



Type: <b><a href="https://msdn.microsoft.com/657439fe-dc17-42af-9e2c-2f3cb769a5a3">D2D1_CREATION_PROPERTIES</a></b>

The filled creation properties structure.



