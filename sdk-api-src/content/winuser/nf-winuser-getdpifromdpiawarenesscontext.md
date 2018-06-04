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

# GetDpiFromDpiAwarenessContext function


## -description


Retrieves the DPI from a given <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> handle. This enables you to determine the DPI of a thread without needed to examine a window created within that thread.


## -parameters




### -param value

TBD




#### - context

The <b>DPI_AWARENESS_CONTEXT</b> handle to examine.


## -returns



The DPI value associated with the <b>DPI_AWARENESS_CONTEXT</b> handle.




## -remarks




<a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> handles associated with values of <b>DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE</b> and <b>DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2</b> will return a value of 0 for their DPI. This is because the DPI of a per-monitor-aware window can change, and the actual DPI cannot be returned without the window's HWND.




## -see-also




<a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a>
 

 

