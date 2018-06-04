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

# IsValidDpiAwarenessContext function


## -description


Determines if a specified <b>DPI_AWARENESS_CONTEXT</b> is valid and supported by the current system.


## -parameters




### -param value [in]

The context that you want to determine if it is supported.


## -returns



<b>TRUE</b> if the provided context is supported, otherwise <b>FALSE</b>.




## -remarks



<b>IsValidDpiAwarenessContext</b> determines the validity of any provided <b>DPI_AWARENESS_CONTEXT</b>. You should make sure a context is valid before using <a href="https://msdn.microsoft.com/95531BDC-3D45-4BB6-8C63-0D845C66B88F">SetThreadDpiAwarenessContext</a> to that context.

An input <i>value</i> of <b>NULL</b> is considered to be an invalid context and will result in a return value of <b>FALSE.</b>



