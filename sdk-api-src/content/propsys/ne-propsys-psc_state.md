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

# PSC_STATE enumeration


## -description


Specifies the state of a property. They are set manually by the code that is hosting the in-memory property store cache.


## -enum-fields




### -field PSC_NORMAL

The property has not been altered.


### -field PSC_NOTINSOURCE

The requested property does not exist for the file or stream on which the property handler was initialized.


### -field PSC_DIRTY

The property has been altered but has not yet been committed to the file or stream.


### -field PSC_READONLY



