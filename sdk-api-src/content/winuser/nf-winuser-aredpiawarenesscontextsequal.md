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

# AreDpiAwarenessContextsEqual function


## -description


Determines whether two <b>DPI_AWARENESS_CONTEXT</b> values are identical.


## -parameters




### -param dpiContextA [in]

The first value to compare.


### -param dpiContextB [in]

The second value to compare.


## -returns



Returns <b>TRUE</b> if the values are equal, otherwise <b>FALSE</b>.




## -remarks



A <b>DPI_AWARENESS_CONTEXT</b> contains multiple pieces of information. For example, it includes both the current and the inherited <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> values. <b>AreDpiAwarenessContextsEqual</b> ignores informational flags and determines if the values are equal. You can't use a direct bitwise comparison because of these informational flags.



