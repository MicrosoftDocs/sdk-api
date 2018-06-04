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

# tagVARKIND enumeration


## -description


Specifies the variable type.


## -enum-fields




### -field VAR_PERINSTANCE

The variable is a field or member of the type. It exists at a fixed offset within each instance of the type.


### -field VAR_STATIC

There is only one instance of the variable.



### -field VAR_CONST

The VARDESC describes a symbolic constant. There is no memory associated with it.



### -field VAR_DISPATCH

The variable can only be accessed through <a href="https://msdn.microsoft.com/964ade8e-9d8a-4d32-bd47-aa678912a54d">IDispatch::Invoke</a>.


