---
UID: NF:d3d12.ID3D12CommandQueue.GetTimestampFrequency
title: ID3D12CommandQueue::GetTimestampFrequency
author: windows-sdk-content
description: This method is used to determine the rate at which the GPU timestamp counter increments.
old-location: direct3d12\id3d12commandqueue_gettimestampfrequency.htm
tech.root: direct3d12
ms.assetid: 90D79775-2898-453E-87FB-CD6850829E47
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetTimestampFrequency, GetTimestampFrequency method, GetTimestampFrequency method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,GetTimestampFrequency method, ID3D12CommandQueue.GetTimestampFrequency, ID3D12CommandQueue::GetTimestampFrequency, d3d12/ID3D12CommandQueue::GetTimestampFrequency, direct3d12.id3d12commandqueue_gettimestampfrequency
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12CommandQueue.GetTimestampFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12CommandQueue::GetTimestampFrequency


## -description


This method is used to determine the rate at which the GPU timestamp counter increments.


## -parameters




### -param pFrequency [out]

Type: <b>UINT64*</b>

The GPU timestamp counter frequency (in ticks/second).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.




## -remarks



For more information, refer to <a href="https://msdn.microsoft.com/CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA">Timing</a>.




## -see-also




<a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>
 

 

