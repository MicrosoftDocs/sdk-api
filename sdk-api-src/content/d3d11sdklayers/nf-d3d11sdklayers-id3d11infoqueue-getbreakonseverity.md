---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetBreakOnSeverity
title: ID3D11InfoQueue::GetBreakOnSeverity
author: windows-sdk-content
description: Get a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d11\id3d11infoqueue_getbreakonseverity.htm
tech.root: direct3d11
ms.assetid: 4023ddb7-006f-46bc-8be8-34ee2bdd9062
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBreakOnSeverity, GetBreakOnSeverity method [Direct3D 11], GetBreakOnSeverity method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetBreakOnSeverity method, ID3D11InfoQueue.GetBreakOnSeverity, ID3D11InfoQueue::GetBreakOnSeverity, d3d11sdklayers/ID3D11InfoQueue::GetBreakOnSeverity, direct3d11.id3d11infoqueue_getbreakonseverity, feb5cad2-8611-d97c-995e-3501a69206d6
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
 - ID3D11InfoQueue.GetBreakOnSeverity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InfoQueue::GetBreakOnSeverity


## -description


Get a message severity level to break on when a message with that severity level passes through the storage filter.


## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a></b>

Message severity level to break on (see <a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Whether this breaking condition is turned on or off (true for on, false for off).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">ID3D11InfoQueue Interface</a>
 

 

