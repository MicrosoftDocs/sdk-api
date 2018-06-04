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

# D3D12_FEATURE_DATA_D3D12_OPTIONS3 structure


## -description


Used to indicate the level of support that the adapter provides for optional features of Direct3D 12.


## -struct-fields




### -field CopyQueueTimestampQueriesSupported


            Indicates whether timestamp queries are supported on copy queues.
          


### -field CastingFullyTypedFormatSupported


            Indicates whether casting from one fully typed format to another, compatible, format is supported.
          


### -field WriteBufferImmediateSupportFlags


            Indicates the kinds of command lists that support the ability to write an immediate value directly from the command stream into a specified buffer.
          


### -field ViewInstancingTier


            Indicates the level of support the adapter has for view instancing.
          


### -field BarycentricsSupported


            Indicates whether barycentrics are supported.
          


## -remarks








## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

