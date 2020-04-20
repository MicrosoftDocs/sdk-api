---
UID: NF:dxgidebug.IDXGIInfoQueue.SetBreakOnCategory
title: IDXGIInfoQueue::SetBreakOnCategory (dxgidebug.h)
description: Sets a message category to break on when a message with that category passes through the storage filter.helpviewer_keywords: ["IDXGIInfoQueue interface [DXGI]","SetBreakOnCategory method","IDXGIInfoQueue.SetBreakOnCategory","IDXGIInfoQueue::SetBreakOnCategory","SetBreakOnCategory","SetBreakOnCategory method [DXGI]","SetBreakOnCategory method [DXGI]","IDXGIInfoQueue interface","direct3ddxgi.idxgiinfoqueue_setbreakoncategory","dxgidebug/IDXGIInfoQueue::SetBreakOnCategory"]
old-location: direct3ddxgi\idxgiinfoqueue_setbreakoncategory.htm
tech.root: direct3ddxgi
ms.assetid: 834C803B-EA7D-4D4C-B74E-9CF7914E0A4E
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],SetBreakOnCategory method, IDXGIInfoQueue.SetBreakOnCategory, IDXGIInfoQueue::SetBreakOnCategory, SetBreakOnCategory, SetBreakOnCategory method [DXGI], SetBreakOnCategory method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_setbreakoncategory, dxgidebug/IDXGIInfoQueue::SetBreakOnCategory
f1_keywords:
- dxgidebug/IDXGIInfoQueue.SetBreakOnCategory
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIInfoQueue::SetBreakOnCategory


## -description


Sets a message category to break on when a message with that category passes through the storage filter.


## -parameters




### -param Producer [in]

 A <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that sets the breaking condition.


### -param Category [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_category">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a>-typed value that specifies the category of the message.


### -param bEnable [in]

A Boolean value that specifies whether <b>SetBreakOnCategory</b> turns on or off this breaking condition (<b>TRUE</b> for on, <b>FALSE</b> for off).


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>
 

 

