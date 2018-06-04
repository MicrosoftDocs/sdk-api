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

# _MI_Server structure


## -description


This structure defines default function tables
 for all types: Context, Instance, PropertySet, and Filter.


## -struct-fields




### -field serverFT

Pointer to an <b>MI_Server</b> function table.


### -field contextFT

Pointer to <a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a> function table.


### -field instanceFT

Pointer to <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> function table.


### -field propertySetFT

Pointer to <a href="https://msdn.microsoft.com/7c9e41b0-818e-46aa-8900-5006904f78d5">MI_PropertySet</a> function table.


### -field filterFT

Pointer to <a href="https://msdn.microsoft.com/0849cb55-ba2f-4855-ac33-fa96d8ecd94f">MI_Filter</a> function table.

