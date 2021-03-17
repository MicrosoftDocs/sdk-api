---
UID: NF:dxgidebug.IDXGIInfoQueue.GetBreakOnCategory
title: IDXGIInfoQueue::GetBreakOnCategory (dxgidebug.h)
description: Determines whether the break on a message category is turned on or off.
helpviewer_keywords: ["GetBreakOnCategory","GetBreakOnCategory method [DXGI]","GetBreakOnCategory method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetBreakOnCategory method","IDXGIInfoQueue.GetBreakOnCategory","IDXGIInfoQueue::GetBreakOnCategory","direct3ddxgi.idxgiinfoqueue_getbreakoncategory","dxgidebug/IDXGIInfoQueue::GetBreakOnCategory"]
old-location: direct3ddxgi\idxgiinfoqueue_getbreakoncategory.htm
tech.root: direct3ddxgi
ms.assetid: 12099FA2-2801-45E7-98C3-5A29F5764B8D
ms.date: 12/05/2018
ms.keywords: GetBreakOnCategory, GetBreakOnCategory method [DXGI], GetBreakOnCategory method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetBreakOnCategory method, IDXGIInfoQueue.GetBreakOnCategory, IDXGIInfoQueue::GetBreakOnCategory, direct3ddxgi.idxgiinfoqueue_getbreakoncategory, dxgidebug/IDXGIInfoQueue::GetBreakOnCategory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIInfoQueue::GetBreakOnCategory
 - dxgidebug/IDXGIInfoQueue::GetBreakOnCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.GetBreakOnCategory
---

# IDXGIInfoQueue::GetBreakOnCategory


## -description

Determines whether the break on a message category is turned on or off.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the breaking status.

### -param Category [in]

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_category">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a>-typed value that specifies the category of the message.

## -returns

Returns a Boolean value that specifies whether this category of breaking condition is turned on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>