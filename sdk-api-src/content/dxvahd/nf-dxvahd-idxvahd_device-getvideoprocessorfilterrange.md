---
UID: NF:dxvahd.IDXVAHD_Device.GetVideoProcessorFilterRange
title: IDXVAHD_Device::GetVideoProcessorFilterRange (dxvahd.h)
description: Gets the range of values for an image filter that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports.
helpviewer_keywords: ["GetVideoProcessorFilterRange","GetVideoProcessorFilterRange method [Media Foundation]","GetVideoProcessorFilterRange method [Media Foundation]","IDXVAHD_Device interface","IDXVAHD_Device interface [Media Foundation]","GetVideoProcessorFilterRange method","IDXVAHD_Device.GetVideoProcessorFilterRange","IDXVAHD_Device::GetVideoProcessorFilterRange","dxvahd/IDXVAHD_Device::GetVideoProcessorFilterRange","mf.idxvahd_device_getvideoprocessorfilterrange"]
old-location: mf\idxvahd_device_getvideoprocessorfilterrange.htm
tech.root: mf
ms.assetid: cff587a5-04ed-4f3e-bd05-0cb8d83fffb7
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorFilterRange, GetVideoProcessorFilterRange method [Media Foundation], GetVideoProcessorFilterRange method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],GetVideoProcessorFilterRange method, IDXVAHD_Device.GetVideoProcessorFilterRange, IDXVAHD_Device::GetVideoProcessorFilterRange, dxvahd/IDXVAHD_Device::GetVideoProcessorFilterRange, mf.idxvahd_device_getvideoprocessorfilterrange
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IDXVAHD_Device::GetVideoProcessorFilterRange
 - dxvahd/IDXVAHD_Device::GetVideoProcessorFilterRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device.GetVideoProcessorFilterRange
---

# IDXVAHD_Device::GetVideoProcessorFilterRange


## -description

Gets the range of values for an image filter that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports.

## -parameters

### -param Filter [in]

The type of image filter, specified as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_filter">DXVAHD_FILTER</a> enumeration.

### -param pRange [out]

A pointer to a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_filter_range_data">DXVAHD_FILTER_RANGE_DATA</a> structure. The method fills the structure with the range of values for the specified filter.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Filter</i> parameter is invalid or the device does not support the specified filter.

</td>
</tr>
</table>

## -remarks

To find out which image filters the device supports, check the <b>FilterCaps</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. Call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method to get this value.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device">IDXVAHD_Device</a>