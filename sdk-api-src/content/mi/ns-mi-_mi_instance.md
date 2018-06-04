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

# _MI_Instance structure


## -description


This structure represents a CIM instance. This object should not be accessed directly. Instead, the 
  <b>MI_Instance_*</b> functions should be used.


## -struct-fields




### -field ft

Pointer to the <a href="https://msdn.microsoft.com/a8cd93b7-c9e0-415e-811a-33826e38417f">MI_InstanceFT</a> function table.


### -field classDecl

The class declaration for this instance.


### -field serverName

Optional server name. Can be null.


### -field nameSpace

Optional namespace. Can be null.


### -field reserved

Reserved for internal use.

