---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.SetBreakOnCategory
title: ID3D12InfoQueue::SetBreakOnCategory (d3d12sdklayers.h)
description: Set a message category to break on when a message with that category passes through the storage filter. (ID3D12InfoQueue.SetBreakOnCategory)
helpviewer_keywords: ["ID3D12InfoQueue interface","SetBreakOnCategory method","ID3D12InfoQueue.SetBreakOnCategory","ID3D12InfoQueue::SetBreakOnCategory","SetBreakOnCategory","SetBreakOnCategory method","SetBreakOnCategory method","ID3D12InfoQueue interface","d3d12sdklayers/ID3D12InfoQueue::SetBreakOnCategory","direct3d12.id3d12infoqueue_setbreakoncategory"]
old-location: direct3d12\id3d12infoqueue_setbreakoncategory.htm
tech.root: direct3d12
ms.assetid: BE56C85A-3FCE-4EC6-B42C-DF0187237AC5
ms.date: 12/05/2018
ms.keywords: ID3D12InfoQueue interface,SetBreakOnCategory method, ID3D12InfoQueue.SetBreakOnCategory, ID3D12InfoQueue::SetBreakOnCategory, SetBreakOnCategory, SetBreakOnCategory method, SetBreakOnCategory method,ID3D12InfoQueue interface, d3d12sdklayers/ID3D12InfoQueue::SetBreakOnCategory, direct3d12.id3d12infoqueue_setbreakoncategory
req.header: d3d12sdklayers.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12InfoQueue::SetBreakOnCategory
 - d3d12sdklayers/ID3D12InfoQueue::SetBreakOnCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.SetBreakOnCategory
---

# ID3D12InfoQueue::SetBreakOnCategory


## -description

Set a message category to break on when a message with that category passes through the storage filter.

## -parameters

### -param Category [in]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category">D3D12_MESSAGE_CATEGORY</a></b>

Message category to break on.

### -param bEnable [in]

Type: <b>BOOL</b>

Turns this breaking condition on or off (true for on, false for off).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
