---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetBreakOnCategory
title: ID3D12InfoQueue::GetBreakOnCategory (d3d12sdklayers.h)
description: Get a message category to break on when a message with that category passes through the storage filter.
helpviewer_keywords: ["GetBreakOnCategory","GetBreakOnCategory method","GetBreakOnCategory method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","GetBreakOnCategory method","ID3D12InfoQueue.GetBreakOnCategory","ID3D12InfoQueue::GetBreakOnCategory","d3d12sdklayers/ID3D12InfoQueue::GetBreakOnCategory","direct3d12.id3d12infoqueue_getbreakoncategory"]
old-location: direct3d12\id3d12infoqueue_getbreakoncategory.htm
tech.root: direct3d12
ms.assetid: 3B966BB5-4AA6-4475-890F-4477A5C7E55E
ms.date: 12/05/2018
ms.keywords: GetBreakOnCategory, GetBreakOnCategory method, GetBreakOnCategory method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetBreakOnCategory method, ID3D12InfoQueue.GetBreakOnCategory, ID3D12InfoQueue::GetBreakOnCategory, d3d12sdklayers/ID3D12InfoQueue::GetBreakOnCategory, direct3d12.id3d12infoqueue_getbreakoncategory
f1_keywords:
- d3d12sdklayers/ID3D12InfoQueue.GetBreakOnCategory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d12sdklayers.h
api_name:
- ID3D12InfoQueue.GetBreakOnCategory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12InfoQueue::GetBreakOnCategory


## -description


Get a message category to break on when a message with that category passes through the storage filter.




## -parameters




### -param Category [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category">D3D12_MESSAGE_CATEGORY</a></b>

Message category to break on.
          


## -returns



Type: <b>BOOL</b>

Whether this breaking condition is turned on or off (true for on, false for off).






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
 

 

