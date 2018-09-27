---
UID: NE:dxgidebug.DXGI_INFO_QUEUE_MESSAGE_CATEGORY
title: DXGI_INFO_QUEUE_MESSAGE_CATEGORY
author: windows-sdk-content
description: Values that specify categories of debug messages.
old-location: direct3ddxgi\dxgi_info_queue_message_category.htm
tech.root: direct3ddxgi
ms.assetid: B7FA9A43-E234-4C2C-832E-69C827F3BA08
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DXGI_INFO_QUEUE_MESSAGE_CATEGORY, DXGI_INFO_QUEUE_MESSAGE_CATEGORY enumeration [DXGI], DXGI_INFO_QUEUE_MESSAGE_CATEGORY_CLEANUP, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_COMPILATION, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_EXECUTION, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_INITIALIZATION, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_MISCELLANEOUS, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_SHADER, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_CREATION, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_GETTING, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_SETTING, DXGI_INFO_QUEUE_MESSAGE_CATEGORY_UNKNOWN, direct3ddxgi.dxgi_info_queue_message_category, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_CLEANUP, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_COMPILATION, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_EXECUTION, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_INITIALIZATION, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_MISCELLANEOUS, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_SHADER, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_CREATION, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_GETTING, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_SETTING, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_CATEGORY_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - DXGI_INFO_QUEUE_MESSAGE_CATEGORY
product: Windows
targetos: Windows
req.typenames: DXGI_INFO_QUEUE_MESSAGE_CATEGORY
req.redist: 
---

# DXGI_INFO_QUEUE_MESSAGE_CATEGORY enumeration


## -description


Values that specify categories of debug messages.


## -enum-fields




### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_UNKNOWN

Unknown category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_MISCELLANEOUS

Miscellaneous category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_INITIALIZATION

Initialization category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_CLEANUP

Cleanup category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_COMPILATION

Compilation category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_CREATION

State creation category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_SETTING

State setting category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_STATE_GETTING

State getting category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_RESOURCE_MANIPULATION

Resource manipulation category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_EXECUTION

Execution category.


### -field DXGI_INFO_QUEUE_MESSAGE_CATEGORY_SHADER

Shader category.


## -remarks



Use this enumeration when you call <a href="https://msdn.microsoft.com/208C3253-09AE-4379-808D-BA0BECC59BF8">IDXGIInfoQueue::GetMessage</a> to retrieve a message and when you call <a href="https://msdn.microsoft.com/965DA310-D082-4970-BCD1-F15F44C074D0">IDXGIInfoQueue::AddMessage</a> to add a message. When you create an info queue filter, you can use these values to allow or deny any categories of messages to pass through the storage and retrieval filters.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

