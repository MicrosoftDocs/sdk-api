---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetBreakOnID
title: ID3D11InfoQueue::SetBreakOnID
author: windows-sdk-content
description: Set a message identifier to break on when a message with that identifier passes through the storage filter.
old-location: direct3d11\id3d11infoqueue_setbreakonid.htm
tech.root: direct3d11
ms.assetid: 7e245c09-bbe1-4601-826b-fe5e71ea6101
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 61b0771c-e26b-3275-edc2-79e49d2f26f0, ID3D11InfoQueue interface [Direct3D 11],SetBreakOnID method, ID3D11InfoQueue.SetBreakOnID, ID3D11InfoQueue::SetBreakOnID, SetBreakOnID, SetBreakOnID method [Direct3D 11], SetBreakOnID method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetBreakOnID, direct3d11.id3d11infoqueue_setbreakonid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.SetBreakOnID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11sdklayers.h
: 
- ID3D11InfoQueue.SetBreakOnID
: 
---

# ID3D11InfoQueue::SetBreakOnID


## -description


Set a message identifier to break on when a message with that identifier passes through the storage filter.


## -parameters




### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476186(v=VS.85).aspx">D3D11_MESSAGE_ID</a></b>

Message identifier to break on (see <a href="https://msdn.microsoft.com/en-us/library/Ff476186(v=VS.85).aspx">D3D11_MESSAGE_ID</a>).


### -param bEnable [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">ID3D11InfoQueue Interface</a>
 

 

