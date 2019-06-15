---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetBreakOnSeverity
title: ID3D12InfoQueue::GetBreakOnSeverity (d3d12sdklayers.h)
author: windows-sdk-content
description: Get a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d12\id3d12infoqueue_getbreakonseverity.htm
tech.root: direct3d12
ms.assetid: 255CB074-9C05-4402-9EDE-43AD8C6707E6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBreakOnSeverity, GetBreakOnSeverity method, GetBreakOnSeverity method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetBreakOnSeverity method, ID3D12InfoQueue.GetBreakOnSeverity, ID3D12InfoQueue::GetBreakOnSeverity, d3d12sdklayers/ID3D12InfoQueue::GetBreakOnSeverity, direct3d12.id3d12infoqueue_getbreakonseverity
ms.topic: method
f1_keywords: ["d3d12sdklayers/ID3D12InfoQueue.GetBreakOnSeverity"]
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
 - ID3D12InfoQueue.GetBreakOnSeverity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12InfoQueue::GetBreakOnSeverity


## -description


Get a message severity level to break on when a message with that severity level passes through the storage filter.




## -parameters




### -param Severity [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity">D3D12_MESSAGE_SEVERITY</a></b>

Message severity level to break on.


## -returns



Type: <b>BOOL</b>

Whether this breaking condition is turned on or off (true for on, false for off).






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
 

 

