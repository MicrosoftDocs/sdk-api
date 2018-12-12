---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetBreakOnSeverity
title: ID3D12InfoQueue::GetBreakOnSeverity
author: windows-sdk-content
description: Get a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d12\id3d12infoqueue_getbreakonseverity.htm
tech.root: direct3d12
ms.assetid: 255CB074-9C05-4402-9EDE-43AD8C6707E6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBreakOnSeverity, GetBreakOnSeverity method, GetBreakOnSeverity method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetBreakOnSeverity method, ID3D12InfoQueue.GetBreakOnSeverity, ID3D12InfoQueue::GetBreakOnSeverity, d3d12sdklayers/ID3D12InfoQueue::GetBreakOnSeverity, direct3d12.id3d12infoqueue_getbreakonseverity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# ID3D12InfoQueue::GetBreakOnSeverity


## -description


Get a message severity level to break on when a message with that severity level passes through the storage filter.




## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/44D94C37-4BA8-49FC-BEEF-6666AD59B627">D3D12_MESSAGE_SEVERITY</a></b>

Message severity level to break on.


## -returns



Type: <b>BOOL</b>

Whether this breaking condition is turned on or off (true for on, false for off).






## -see-also




<a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>
 

 

