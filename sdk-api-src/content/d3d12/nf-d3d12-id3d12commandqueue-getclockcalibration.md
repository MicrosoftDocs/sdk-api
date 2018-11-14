---
UID: NF:d3d12.ID3D12CommandQueue.GetClockCalibration
title: ID3D12CommandQueue::GetClockCalibration
author: windows-sdk-content
description: This method samples the CPU and GPU timestamp counters at the same moment in time.
old-location: direct3d12\id3d12commandqueue_getclockcalibration.htm
tech.root: direct3d12
ms.assetid: B8E0F8D4-D291-41B5-8E40-0C1FB3DCC253
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetClockCalibration, GetClockCalibration method, GetClockCalibration method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,GetClockCalibration method, ID3D12CommandQueue.GetClockCalibration, ID3D12CommandQueue::GetClockCalibration, d3d12/ID3D12CommandQueue::GetClockCalibration, direct3d12.id3d12commandqueue_getclockcalibration
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
 - ID3D12CommandQueue.GetClockCalibration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12.h
: 
- ID3D12CommandQueue.GetClockCalibration
: 
---

# ID3D12CommandQueue::GetClockCalibration


## -description


This method samples the CPU and GPU timestamp counters at the same moment in time. 


## -parameters




### -param pGpuTimestamp [out]

Type: <b>UINT64*</b>

The value of the GPU timestamp counter.


### -param pCpuTimestamp [out]

Type: <b>UINT64*</b>

The value of the CPU timestamp counter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.




## -remarks



For more information, refer to <a href="https://msdn.microsoft.com/CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA">Timing</a>.




## -see-also




<a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>
 

 

