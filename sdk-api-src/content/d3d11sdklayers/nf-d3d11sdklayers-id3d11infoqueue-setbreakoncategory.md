---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetBreakOnCategory
title: ID3D11InfoQueue::SetBreakOnCategory (d3d11sdklayers.h)
description: Set a message category to break on when a message with that category passes through the storage filter. (ID3D11InfoQueue.SetBreakOnCategory)
helpviewer_keywords: ["17afaa7e-0f5c-964c-84e9-887599f0d947","ID3D11InfoQueue interface [Direct3D 11]","SetBreakOnCategory method","ID3D11InfoQueue.SetBreakOnCategory","ID3D11InfoQueue::SetBreakOnCategory","SetBreakOnCategory","SetBreakOnCategory method [Direct3D 11]","SetBreakOnCategory method [Direct3D 11]","ID3D11InfoQueue interface","d3d11sdklayers/ID3D11InfoQueue::SetBreakOnCategory","direct3d11.id3d11infoqueue_setbreakoncategory"]
old-location: direct3d11\id3d11infoqueue_setbreakoncategory.htm
tech.root: direct3d11
ms.assetid: 3d6f66bf-01b8-4bab-a40e-98f5893050cd
ms.date: 12/05/2018
ms.keywords: 17afaa7e-0f5c-964c-84e9-887599f0d947, ID3D11InfoQueue interface [Direct3D 11],SetBreakOnCategory method, ID3D11InfoQueue.SetBreakOnCategory, ID3D11InfoQueue::SetBreakOnCategory, SetBreakOnCategory, SetBreakOnCategory method [Direct3D 11], SetBreakOnCategory method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetBreakOnCategory, direct3d11.id3d11infoqueue_setbreakoncategory
req.header: d3d11sdklayers.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11InfoQueue::SetBreakOnCategory
 - d3d11sdklayers/ID3D11InfoQueue::SetBreakOnCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.SetBreakOnCategory
---

# ID3D11InfoQueue::SetBreakOnCategory


## -description

Set a message category to break on when a message with that category passes through the storage filter.

## -parameters

### -param Category [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_category">D3D11_MESSAGE_CATEGORY</a></b>

Message category to break on (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_category">D3D11_MESSAGE_CATEGORY</a>).

### -param bEnable [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
