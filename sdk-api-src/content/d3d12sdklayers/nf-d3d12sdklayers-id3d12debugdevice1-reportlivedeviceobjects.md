---
UID: NF:d3d12sdklayers.ID3D12DebugDevice1.ReportLiveDeviceObjects
title: ID3D12DebugDevice1::ReportLiveDeviceObjects
author: windows-sdk-content
description: Specifies the amount of information to report on a device object's lifetime.
old-location: direct3d12\id3d12debugdevice1_reportlivedeviceobjects.htm
old-project: direct3d12
ms.assetid: 99895407-2BFF-40AA-BAE4-C304295DA0E4
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12DebugDevice1 interface,ReportLiveDeviceObjects method, ID3D12DebugDevice1.ReportLiveDeviceObjects, ID3D12DebugDevice1::ReportLiveDeviceObjects, ReportLiveDeviceObjects, ReportLiveDeviceObjects method, ReportLiveDeviceObjects method,ID3D12DebugDevice1 interface, d3d12sdklayers/ID3D12DebugDevice1::ReportLiveDeviceObjects, direct3d12.id3d12debugdevice1_reportlivedeviceobjects
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugDevice1.ReportLiveDeviceObjects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12DebugDevice1::ReportLiveDeviceObjects


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Specifies the amount of information to report  on a device object's lifetime.


## -parameters




### -param Flags

Type: <b><a href="https://msdn.microsoft.com/FF868102-26FC-4541-9C21-0B8D6D4CF47B">D3D12_RLDO_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/FF868102-26FC-4541-9C21-0B8D6D4CF47B">D3D12_RLDO_FLAGS</a> enumeration. This method uses the value in <i>Flags</i> to determine the amount of information to report about a device object's lifetime.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/DDB71272-195A-4E05-BA52-9EF858ACD6CB">ID3D12DebugDevice1</a>
 

 

