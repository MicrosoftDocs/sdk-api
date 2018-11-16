---
UID: NF:dxgidebug.IDXGIInfoQueue.GetBreakOnCategory
title: IDXGIInfoQueue::GetBreakOnCategory
author: windows-sdk-content
description: Determines whether the break on a message category is turned on or off.
old-location: direct3ddxgi\idxgiinfoqueue_getbreakoncategory.htm
tech.root: direct3ddxgi
ms.assetid: 12099FA2-2801-45E7-98C3-5A29F5764B8D
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetBreakOnCategory, GetBreakOnCategory method [DXGI], GetBreakOnCategory method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetBreakOnCategory method, IDXGIInfoQueue.GetBreakOnCategory, IDXGIInfoQueue::GetBreakOnCategory, direct3ddxgi.idxgiinfoqueue_getbreakoncategory, dxgidebug/IDXGIInfoQueue::GetBreakOnCategory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.dll: DXGIDebug.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.GetBreakOnCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgidebug.h
: 
- IDXGIInfoQueue.GetBreakOnCategory
: 
---

# IDXGIInfoQueue::GetBreakOnCategory


## -description


Determines whether the break on a message category is turned on or off.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the breaking status.


### -param Category [in]

A <a href="https://msdn.microsoft.com/B7FA9A43-E234-4C2C-832E-69C827F3BA08">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a>-typed value that specifies the category of the message.


## -returns



Returns a Boolean value that specifies whether this category of breaking condition is turned on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

