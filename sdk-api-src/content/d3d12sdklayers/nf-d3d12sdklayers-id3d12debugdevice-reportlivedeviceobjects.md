---
UID: NF:d3d12sdklayers.ID3D12DebugDevice.ReportLiveDeviceObjects
title: ID3D12DebugDevice::ReportLiveDeviceObjects
author: windows-sdk-content
description: Reports information about a device object's lifetime.
old-location: direct3d12\id3d12debugdevice_reportlivedeviceobjects.htm
tech.root: direct3d12
ms.assetid: 37771598-DC2E-42FA-B17D-A187164A3314
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D12DebugDevice interface,ReportLiveDeviceObjects method, ID3D12DebugDevice.ReportLiveDeviceObjects, ID3D12DebugDevice::ReportLiveDeviceObjects, ReportLiveDeviceObjects, ReportLiveDeviceObjects method, ReportLiveDeviceObjects method,ID3D12DebugDevice interface, d3d12sdklayers/ID3D12DebugDevice::ReportLiveDeviceObjects, direct3d12.id3d12debugdevice_reportlivedeviceobjects
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
 - ID3D12DebugDevice.ReportLiveDeviceObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12sdklayers.h
: 
- ID3D12DebugDevice.ReportLiveDeviceObjects
: 
---

# ID3D12DebugDevice::ReportLiveDeviceObjects


## -description


Reports information about a device object's lifetime.
        


## -parameters




### -param Flags

Type: <b><a href="https://msdn.microsoft.com/FF868102-26FC-4541-9C21-0B8D6D4CF47B">D3D12_RLDO_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/FF868102-26FC-4541-9C21-0B8D6D4CF47B">D3D12_RLDO_FLAGS</a> enumeration.
            This method uses the value in <i>Flags</i> to determine the amount of information to report about a device object's lifetime.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
            <a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a>





## -see-also




<a href="https://msdn.microsoft.com/6FD77F14-E260-4DBB-8434-664DE1F6DE39">ID3D12DebugDevice</a>
 

 

