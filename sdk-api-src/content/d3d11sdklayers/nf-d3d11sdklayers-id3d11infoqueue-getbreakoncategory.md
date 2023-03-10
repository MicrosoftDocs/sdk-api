---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetBreakOnCategory
title: ID3D11InfoQueue::GetBreakOnCategory (d3d11sdklayers.h)
description: Get a message category to break on when a message with that category passes through the storage filter. (ID3D11InfoQueue.GetBreakOnCategory)
helpviewer_keywords: ["08043309-7517-83fc-be14-01f7cb816e88","GetBreakOnCategory","GetBreakOnCategory method [Direct3D 11]","GetBreakOnCategory method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","GetBreakOnCategory method","ID3D11InfoQueue.GetBreakOnCategory","ID3D11InfoQueue::GetBreakOnCategory","d3d11sdklayers/ID3D11InfoQueue::GetBreakOnCategory","direct3d11.id3d11infoqueue_getbreakoncategory"]
old-location: direct3d11\id3d11infoqueue_getbreakoncategory.htm
tech.root: direct3d11
ms.assetid: 747755ec-3260-4ded-9c36-efdf1a90adcb
ms.date: 12/05/2018
ms.keywords: 08043309-7517-83fc-be14-01f7cb816e88, GetBreakOnCategory, GetBreakOnCategory method [Direct3D 11], GetBreakOnCategory method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetBreakOnCategory method, ID3D11InfoQueue.GetBreakOnCategory, ID3D11InfoQueue::GetBreakOnCategory, d3d11sdklayers/ID3D11InfoQueue::GetBreakOnCategory, direct3d11.id3d11infoqueue_getbreakoncategory
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
 - ID3D11InfoQueue::GetBreakOnCategory
 - d3d11sdklayers/ID3D11InfoQueue::GetBreakOnCategory
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
 - ID3D11InfoQueue.GetBreakOnCategory
---

# ID3D11InfoQueue::GetBreakOnCategory


## -description

Get a message category to break on when a message with that category passes through the storage filter.

## -parameters

### -param Category [in]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_category">D3D11_MESSAGE_CATEGORY</a></b>

Message category to break on (see <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_message_category">D3D11_MESSAGE_CATEGORY</a>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
