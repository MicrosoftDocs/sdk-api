---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetBreakOnID
title: ID3D10InfoQueue::GetBreakOnID
author: windows-sdk-content
description: Get a message identifier to break on when a message with that identifier passes through the storage filter.
old-location: direct3d10\id3d10infoqueue_getbreakonid.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getbreakonid.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetBreakOnID, GetBreakOnID method [Direct3D 10], GetBreakOnID method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetBreakOnID method, ID3D10InfoQueue.GetBreakOnID, ID3D10InfoQueue::GetBreakOnID, ce099e0a-fe76-1548-a605-708bb35400d4, d3d10sdklayers/ID3D10InfoQueue::GetBreakOnID, direct3d10.id3d10infoqueue_getbreakonid
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.GetBreakOnID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::GetBreakOnID


## -description


Get a message identifier to break on when a message with that identifier passes through the storage filter.


## -parameters




### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb205324(v=VS.85).aspx">D3D10_MESSAGE_ID</a></b>

Message identifier to break on (see <a href="https://msdn.microsoft.com/library/Bb205324(v=VS.85).aspx">D3D10_MESSAGE_ID</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173779(v=VS.85).aspx">ID3D10InfoQueue Interface</a>
 

 

