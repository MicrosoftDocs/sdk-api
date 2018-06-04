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

# ResUtilSetValueEx function


## -description


Sets a value in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

A key that identifies the location of the value in the cluster database.


### -param valueName [in]

A Null-terminated Unicode string that contains the name of the value to update.


### -param valueType [in]

A flag that indicates the type of the value to update.


### -param valueData [in]

A pointer to the new data for the value.


### -param valueSize [in]

The size of the new value, in bytes.


### -param flags [in]

The flags that specify settings for the operation.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation succeeds; otherwise, returns a system error code.



