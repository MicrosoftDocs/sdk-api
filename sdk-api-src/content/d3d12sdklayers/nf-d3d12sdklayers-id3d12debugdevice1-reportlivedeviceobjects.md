---
UID: NF:d3d12sdklayers.ID3D12DebugDevice1.ReportLiveDeviceObjects
title: ID3D12DebugDevice1::ReportLiveDeviceObjects (d3d12sdklayers.h)
description: Specifies the amount of information to report on a device object's lifetime.
helpviewer_keywords: ["ID3D12DebugDevice1 interface","ReportLiveDeviceObjects method","ID3D12DebugDevice1.ReportLiveDeviceObjects","ID3D12DebugDevice1::ReportLiveDeviceObjects","ReportLiveDeviceObjects","ReportLiveDeviceObjects method","ReportLiveDeviceObjects method","ID3D12DebugDevice1 interface","d3d12sdklayers/ID3D12DebugDevice1::ReportLiveDeviceObjects","direct3d12.id3d12debugdevice1_reportlivedeviceobjects"]
old-location: direct3d12\id3d12debugdevice1_reportlivedeviceobjects.htm
tech.root: direct3d12
ms.assetid: 99895407-2BFF-40AA-BAE4-C304295DA0E4
ms.date: 12/05/2018
ms.keywords: ID3D12DebugDevice1 interface,ReportLiveDeviceObjects method, ID3D12DebugDevice1.ReportLiveDeviceObjects, ID3D12DebugDevice1::ReportLiveDeviceObjects, ReportLiveDeviceObjects, ReportLiveDeviceObjects method, ReportLiveDeviceObjects method,ID3D12DebugDevice1 interface, d3d12sdklayers/ID3D12DebugDevice1::ReportLiveDeviceObjects, direct3d12.id3d12debugdevice1_reportlivedeviceobjects
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
 - ID3D12DebugDevice1::ReportLiveDeviceObjects
 - d3d12sdklayers/ID3D12DebugDevice1::ReportLiveDeviceObjects
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
 - ID3D12DebugDevice1.ReportLiveDeviceObjects
---

# ID3D12DebugDevice1::ReportLiveDeviceObjects


## -description

Specifies the amount of information to report  on a device object's lifetime.

## -parameters

### -param Flags

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags">D3D12_RLDO_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags">D3D12_RLDO_FLAGS</a> enumeration. This method uses the value in <i>Flags</i> to determine the amount of information to report about a device object's lifetime.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1">ID3D12DebugDevice1</a>