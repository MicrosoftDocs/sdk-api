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

# DXGI_INFO_QUEUE_FILTER structure


## -description


Describes a debug message filter, which contains lists of message types to allow and deny.


## -struct-fields




### -field AllowList

A <a href="https://msdn.microsoft.com/B916731B-362B-46AD-BC18-71339A2935B4">DXGI_INFO_QUEUE_FILTER_DESC</a> structure that describes the types of messages to allow.


### -field DenyList

A <a href="https://msdn.microsoft.com/B916731B-362B-46AD-BC18-71339A2935B4">DXGI_INFO_QUEUE_FILTER_DESC</a> structure that describes the types of messages to deny.


## -remarks



Use with an <a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a> interface.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

