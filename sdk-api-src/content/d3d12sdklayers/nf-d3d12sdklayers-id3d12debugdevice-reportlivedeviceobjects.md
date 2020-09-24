---
UID: NF:d3d12sdklayers.ID3D12DebugDevice.ReportLiveDeviceObjects
title: ID3D12DebugDevice::ReportLiveDeviceObjects (d3d12sdklayers.h)
description: Reports information about a device object's lifetime.
helpviewer_keywords: ["ID3D12DebugDevice interface","ReportLiveDeviceObjects method","ID3D12DebugDevice.ReportLiveDeviceObjects","ID3D12DebugDevice::ReportLiveDeviceObjects","ReportLiveDeviceObjects","ReportLiveDeviceObjects method","ReportLiveDeviceObjects method","ID3D12DebugDevice interface","d3d12sdklayers/ID3D12DebugDevice::ReportLiveDeviceObjects","direct3d12.id3d12debugdevice_reportlivedeviceobjects"]
old-location: direct3d12\id3d12debugdevice_reportlivedeviceobjects.htm
tech.root: direct3d12
ms.assetid: 37771598-DC2E-42FA-B17D-A187164A3314
ms.date: 12/05/2018
ms.keywords: ID3D12DebugDevice interface,ReportLiveDeviceObjects method, ID3D12DebugDevice.ReportLiveDeviceObjects, ID3D12DebugDevice::ReportLiveDeviceObjects, ReportLiveDeviceObjects, ReportLiveDeviceObjects method, ReportLiveDeviceObjects method,ID3D12DebugDevice interface, d3d12sdklayers/ID3D12DebugDevice::ReportLiveDeviceObjects, direct3d12.id3d12debugdevice_reportlivedeviceobjects
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12DebugDevice::ReportLiveDeviceObjects
 - d3d12sdklayers/ID3D12DebugDevice::ReportLiveDeviceObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugDevice.ReportLiveDeviceObjects
---

# ID3D12DebugDevice::ReportLiveDeviceObjects


## -description

Reports information about a device object's lifetime.

## -parameters

### -param Flags

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags">D3D12_RLDO_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags">D3D12_RLDO_FLAGS</a> enumeration.
            This method uses the value in <i>Flags</i> to determine the amount of information to report about a device object's lifetime.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.
            <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a>

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice">ID3D12DebugDevice</a>