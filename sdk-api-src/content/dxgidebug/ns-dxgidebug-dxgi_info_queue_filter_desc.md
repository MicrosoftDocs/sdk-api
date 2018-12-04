---
UID: NS:dxgidebug.DXGI_INFO_QUEUE_FILTER_DESC
title: DXGI_INFO_QUEUE_FILTER_DESC
author: windows-sdk-content
description: Describes the types of messages to allow or deny to pass through a filter.
old-location: direct3ddxgi\dxgi_info_queue_filter_desc.htm
tech.root: direct3ddxgi
ms.assetid: B916731B-362B-46AD-BC18-71339A2935B4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DXGI_INFO_QUEUE_FILTER_DESC, DXGI_INFO_QUEUE_FILTER_DESC structure [DXGI], direct3ddxgi.dxgi_info_queue_filter_desc, dxgidebug/DXGI_INFO_QUEUE_FILTER_DESC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxgidebug.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGIDebug.h
api_name:
 - DXGI_INFO_QUEUE_FILTER_DESC
product: Windows
targetos: Windows
req.typenames: DXGI_INFO_QUEUE_FILTER_DESC
req.redist: 
---

# DXGI_INFO_QUEUE_FILTER_DESC structure


## -description


Describes the types of messages to allow or deny to pass through a filter.


## -struct-fields




### -field NumCategories

The number of message categories to allow or deny.


### -field pCategoryList

An array of <a href="https://msdn.microsoft.com/B7FA9A43-E234-4C2C-832E-69C827F3BA08">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a> enumeration values that describe the message categories to allow or deny. The array must have at least <b>NumCategories</b> number of elements.


### -field NumSeverities

The number of message severity levels to allow or deny.


### -field pSeverityList

An array of <a href="https://msdn.microsoft.com/99F9DDC8-5CCF-4991-94AD-0A399932F5B3">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a> enumeration values that describe the message severity levels to allow or deny. The array must have at least <b>NumSeverities</b> number of elements.


### -field NumIDs

The number of message IDs to allow or deny.


### -field pIDList

An array of integers that represent the message IDs to allow or deny. The array must have at least <b>NumIDs</b> number of elements.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/95E68ECE-39D2-4D16-9A8F-FE6E527A83E3">DXGI_INFO_QUEUE_FILTER</a> structure.

This API requires the Windows Software Development Kit (SDK) for Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

