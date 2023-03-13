---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetBreakOnCategory
title: ID3D10InfoQueue::GetBreakOnCategory (d3d10sdklayers.h)
description: Get a message category to break on when a message with that category passes through the storage filter. (ID3D10InfoQueue.GetBreakOnCategory)
helpviewer_keywords: ["GetBreakOnCategory","GetBreakOnCategory method [Direct3D 10]","GetBreakOnCategory method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","GetBreakOnCategory method","ID3D10InfoQueue.GetBreakOnCategory","ID3D10InfoQueue::GetBreakOnCategory","d3d10sdklayers/ID3D10InfoQueue::GetBreakOnCategory","direct3d10.id3d10infoqueue_getbreakoncategory","f7712289-f56a-df8e-a2dd-2568f07262a8"]
old-location: direct3d10\id3d10infoqueue_getbreakoncategory.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getbreakoncategory.htm
ms.date: 12/05/2018
ms.keywords: GetBreakOnCategory, GetBreakOnCategory method [Direct3D 10], GetBreakOnCategory method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetBreakOnCategory method, ID3D10InfoQueue.GetBreakOnCategory, ID3D10InfoQueue::GetBreakOnCategory, d3d10sdklayers/ID3D10InfoQueue::GetBreakOnCategory, direct3d10.id3d10infoqueue_getbreakoncategory, f7712289-f56a-df8e-a2dd-2568f07262a8
req.header: d3d10sdklayers.h
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
 - ID3D10InfoQueue::GetBreakOnCategory
 - d3d10sdklayers/ID3D10InfoQueue::GetBreakOnCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.GetBreakOnCategory
---

# ID3D10InfoQueue::GetBreakOnCategory


## -description

Get a message category to break on when a message with that category passes through the storage filter.

## -parameters

### -param Category [in]

Type: <b><a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category">D3D10_MESSAGE_CATEGORY</a></b>

Message category to break on (see <a href="/windows/desktop/api/d3d10sdklayers/ne-d3d10sdklayers-d3d10_message_category">D3D10_MESSAGE_CATEGORY</a>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
