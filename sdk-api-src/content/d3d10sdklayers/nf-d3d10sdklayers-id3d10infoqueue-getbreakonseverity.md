---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetBreakOnSeverity
title: ID3D10InfoQueue::GetBreakOnSeverity
author: windows-sdk-content
description: Get a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d10\id3d10infoqueue_getbreakonseverity.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getbreakonseverity.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 640ea84e-c7af-c3d2-d27b-1edd4a3629f9, GetBreakOnSeverity, GetBreakOnSeverity method [Direct3D 10], GetBreakOnSeverity method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetBreakOnSeverity method, ID3D10InfoQueue.GetBreakOnSeverity, ID3D10InfoQueue::GetBreakOnSeverity, d3d10sdklayers/ID3D10InfoQueue::GetBreakOnSeverity, direct3d10.id3d10infoqueue_getbreakonseverity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.GetBreakOnSeverity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10sdklayers.h
: 
- ID3D10InfoQueue.GetBreakOnSeverity
: 
---

# ID3D10InfoQueue::GetBreakOnSeverity


## -description


Get a message severity level to break on when a message with that severity level passes through the storage filter.


## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/548487cb-1315-45b2-86df-f32d129a1212">D3D10_MESSAGE_SEVERITY</a></b>

Message severity level to break on (see <a href="https://msdn.microsoft.com/548487cb-1315-45b2-86df-f32d129a1212">D3D10_MESSAGE_SEVERITY</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

