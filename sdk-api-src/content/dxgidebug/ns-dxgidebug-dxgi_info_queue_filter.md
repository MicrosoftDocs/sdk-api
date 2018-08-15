---
UID: NS:dxgidebug.DXGI_INFO_QUEUE_FILTER
title: DXGI_INFO_QUEUE_FILTER
author: windows-sdk-content
description: Describes a debug message filter, which contains lists of message types to allow and deny.
old-location: direct3ddxgi\dxgi_info_queue_filter.htm
old-project: direct3ddxgi
ms.assetid: 95E68ECE-39D2-4D16-9A8F-FE6E527A83E3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DXGI_INFO_QUEUE_FILTER, DXGI_INFO_QUEUE_FILTER structure [DXGI], direct3ddxgi.dxgi_info_queue_filter, dxgidebug/DXGI_INFO_QUEUE_FILTER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgidebug.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DXGI_INFO_QUEUE_FILTER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGIDebug.h
api_name:
 - DXGI_INFO_QUEUE_FILTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

