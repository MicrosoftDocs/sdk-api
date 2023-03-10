---
UID: NF:dxgidebug.IDXGIInfoQueue.GetBreakOnID
title: IDXGIInfoQueue::GetBreakOnID (dxgidebug.h)
description: Determines whether the break on a message identifier is turned on or off.
helpviewer_keywords: ["GetBreakOnID","GetBreakOnID method [DXGI]","GetBreakOnID method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetBreakOnID method","IDXGIInfoQueue.GetBreakOnID","IDXGIInfoQueue::GetBreakOnID","direct3ddxgi.idxgiinfoqueue_getbreakonid","dxgidebug/IDXGIInfoQueue::GetBreakOnID"]
old-location: direct3ddxgi\idxgiinfoqueue_getbreakonid.htm
tech.root: direct3ddxgi
ms.assetid: A7DF79E0-137D-4CBD-AD03-B9BC4532D60F
ms.date: 12/05/2018
ms.keywords: GetBreakOnID, GetBreakOnID method [DXGI], GetBreakOnID method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetBreakOnID method, IDXGIInfoQueue.GetBreakOnID, IDXGIInfoQueue::GetBreakOnID, direct3ddxgi.idxgiinfoqueue_getbreakonid, dxgidebug/IDXGIInfoQueue::GetBreakOnID
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
 - IDXGIInfoQueue::GetBreakOnID
 - dxgidebug/IDXGIInfoQueue::GetBreakOnID
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
 - IDXGIInfoQueue.GetBreakOnID
---

# IDXGIInfoQueue::GetBreakOnID


## -description

Determines whether the break on a message identifier is turned on or off.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the breaking status.

### -param ID [in]

An integer value that specifies the identifier of the message.

## -returns

Returns a Boolean value that specifies whether this break on a message identifier is turned on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>