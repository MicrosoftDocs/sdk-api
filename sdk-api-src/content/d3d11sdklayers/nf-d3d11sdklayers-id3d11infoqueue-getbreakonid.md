---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetBreakOnID
title: ID3D11InfoQueue::GetBreakOnID
author: windows-sdk-content
description: Get a message identifier to break on when a message with that identifier passes through the storage filter.
old-location: direct3d11\id3d11infoqueue_getbreakonid.htm
old-project: direct3d11
ms.assetid: 0efccfd5-55ec-4151-81ca-fe826f44adaa
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetBreakOnID, GetBreakOnID method [Direct3D 11], GetBreakOnID method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetBreakOnID method, ID3D11InfoQueue.GetBreakOnID, ID3D11InfoQueue::GetBreakOnID, d3d11sdklayers/ID3D11InfoQueue::GetBreakOnID, dd404ca7-c714-15ae-464b-cc6080192960, direct3d11.id3d11infoqueue_getbreakonid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.GetBreakOnID
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue::GetBreakOnID


## -description


Get a message identifier to break on when a message with that identifier passes through the storage filter.


## -parameters




### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/50dde92d-9856-4010-8848-485a8d92b145">D3D11_MESSAGE_ID</a></b>

Message identifier to break on (see <a href="https://msdn.microsoft.com/50dde92d-9856-4010-8848-485a8d92b145">D3D11_MESSAGE_ID</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

