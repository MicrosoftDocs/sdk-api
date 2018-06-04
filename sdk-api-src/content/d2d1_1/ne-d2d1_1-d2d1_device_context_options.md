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

# D2D1_DEVICE_CONTEXT_OPTIONS enumeration


## -description


This specifies options that apply to the device context for its lifetime.


## -enum-fields




### -field D2D1_DEVICE_CONTEXT_OPTIONS_NONE

The device context is created with default options.


### -field D2D1_DEVICE_CONTEXT_OPTIONS_ENABLE_MULTITHREADED_OPTIMIZATIONS

Distribute rendering work across multiple threads. Refer to <a href="http://msdn.microsoft.com/en-us/library/windows/desktop/dd372260(v=vs.85).aspx">Improving the performance of Direct2D apps</a> for additional notes on the use of this flag.


### -field D2D1_DEVICE_CONTEXT_OPTIONS_FORCE_DWORD



