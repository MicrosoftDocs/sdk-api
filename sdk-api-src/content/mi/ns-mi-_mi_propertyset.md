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

# _MI_PropertySet structure


## -description


Implements a set of property names.


## -struct-fields




### -field ft

Pointer to the <a href="https://msdn.microsoft.com/d71c0378-0b97-44ea-9f42-e533b93f195e">MI_PropertySetFT</a> function table.


### -field reserved

Reserved for internal use.


## -remarks



It supports the building and interrogation of property sets. In general, clients  build property sets and providers interrogate them.



