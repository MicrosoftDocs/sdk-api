---
UID: NS:dxgidebug.DXGI_INFO_QUEUE_MESSAGE
title: DXGI_INFO_QUEUE_MESSAGE
author: windows-sdk-content
description: Describes a debug message in the information queue.
old-location: direct3ddxgi\dxgi_info_queue_message.htm
tech.root: direct3ddxgi
ms.assetid: F0FF1DC6-8E62-4D35-BCB7-EC3BB314F033
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DXGI_INFO_QUEUE_MESSAGE, DXGI_INFO_QUEUE_MESSAGE structure [DXGI], direct3ddxgi.dxgi_info_queue_message, dxgidebug/DXGI_INFO_QUEUE_MESSAGE
ms.prod: windows
ms.technology: windows-sdk
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
 - DXGI_INFO_QUEUE_MESSAGE
product: Windows
targetos: Windows
req.typenames: DXGI_INFO_QUEUE_MESSAGE
req.redist: 
---

# DXGI_INFO_QUEUE_MESSAGE structure


## -description


Describes a debug message in the information queue.


## -struct-fields




### -field Producer

A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that produced the message.


### -field Category

A <a href="https://msdn.microsoft.com/B7FA9A43-E234-4C2C-832E-69C827F3BA08">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a>-typed value that specifies the category of the message.


### -field Severity

A <a href="https://msdn.microsoft.com/99F9DDC8-5CCF-4991-94AD-0A399932F5B3">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.


### -field ID

An integer that uniquely identifies the message.


### -field pDescription

The message string.


### -field DescriptionByteLength

The length of the message string at <b>pDescription</b>, in bytes.


## -remarks




<a href="https://msdn.microsoft.com/208C3253-09AE-4379-808D-BA0BECC59BF8">IDXGIInfoQueue::GetMessage</a> returns a pointer to this structure.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

