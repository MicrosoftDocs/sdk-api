---
UID: NF:dxgidebug.IDXGIInfoQueue.SetBreakOnCategory
title: IDXGIInfoQueue::SetBreakOnCategory
author: windows-sdk-content
description: Sets a message category to break on when a message with that category passes through the storage filter.
old-location: direct3ddxgi\idxgiinfoqueue_setbreakoncategory.htm
tech.root: direct3ddxgi
ms.assetid: 834C803B-EA7D-4D4C-B74E-9CF7914E0A4E
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],SetBreakOnCategory method, IDXGIInfoQueue.SetBreakOnCategory, IDXGIInfoQueue::SetBreakOnCategory, SetBreakOnCategory, SetBreakOnCategory method [DXGI], SetBreakOnCategory method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_setbreakoncategory, dxgidebug/IDXGIInfoQueue::SetBreakOnCategory
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
 - IDXGIInfoQueue.SetBreakOnCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIInfoQueue::SetBreakOnCategory


## -description


Sets a message category to break on when a message with that category passes through the storage filter.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that sets the breaking condition.


### -param Category [in]

A <a href="https://msdn.microsoft.com/B7FA9A43-E234-4C2C-832E-69C827F3BA08">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a>-typed value that specifies the category of the message.


### -param bEnable [in]

A Boolean value that specifies whether <b>SetBreakOnCategory</b> turns on or off this breaking condition (<b>TRUE</b> for on, <b>FALSE</b> for off).


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

