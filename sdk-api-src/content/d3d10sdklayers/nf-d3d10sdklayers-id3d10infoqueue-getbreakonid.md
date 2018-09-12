---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetBreakOnID
title: ID3D10InfoQueue::GetBreakOnID
author: windows-sdk-content
description: Get a message identifier to break on when a message with that identifier passes through the storage filter.
old-location: direct3d10\id3d10infoqueue_getbreakonid.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getbreakonid.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetBreakOnID, GetBreakOnID method [Direct3D 10], GetBreakOnID method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetBreakOnID method, ID3D10InfoQueue.GetBreakOnID, ID3D10InfoQueue::GetBreakOnID, ce099e0a-fe76-1548-a605-708bb35400d4, d3d10sdklayers/ID3D10InfoQueue::GetBreakOnID, direct3d10.id3d10infoqueue_getbreakonid
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
 - ID3D10InfoQueue.GetBreakOnID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10InfoQueue::GetBreakOnID


## -description


Get a message identifier to break on when a message with that identifier passes through the storage filter.


## -parameters




### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/c5c07158-d102-4064-94e7-eecf8b60ac98">D3D10_MESSAGE_ID</a></b>

Message identifier to break on (see <a href="https://msdn.microsoft.com/c5c07158-d102-4064-94e7-eecf8b60ac98">D3D10_MESSAGE_ID</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

