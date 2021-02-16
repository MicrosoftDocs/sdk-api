---
UID: NF:dxva2api.IDirectXVideoProcessor.GetFilterPropertyRange
title: IDirectXVideoProcessor::GetFilterPropertyRange (dxva2api.h)
description: Retrieves the range of values for an image filter supported by this device.
helpviewer_keywords: ["550c426b-a194-4ed6-9a90-b79a93e79322","GetFilterPropertyRange","GetFilterPropertyRange method [Media Foundation]","GetFilterPropertyRange method [Media Foundation]","IDirectXVideoProcessor interface","IDirectXVideoProcessor interface [Media Foundation]","GetFilterPropertyRange method","IDirectXVideoProcessor.GetFilterPropertyRange","IDirectXVideoProcessor::GetFilterPropertyRange","dxva2api/IDirectXVideoProcessor::GetFilterPropertyRange","mf.idirectxvideoprocessor_getfilterpropertyrange"]
old-location: mf\idirectxvideoprocessor_getfilterpropertyrange.htm
tech.root: mf
ms.assetid: 550c426b-a194-4ed6-9a90-b79a93e79322
ms.date: 12/05/2018
ms.keywords: 550c426b-a194-4ed6-9a90-b79a93e79322, GetFilterPropertyRange, GetFilterPropertyRange method [Media Foundation], GetFilterPropertyRange method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetFilterPropertyRange method, IDirectXVideoProcessor.GetFilterPropertyRange, IDirectXVideoProcessor::GetFilterPropertyRange, dxva2api/IDirectXVideoProcessor::GetFilterPropertyRange, mf.idirectxvideoprocessor_getfilterpropertyrange
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IDirectXVideoProcessor::GetFilterPropertyRange
 - dxva2api/IDirectXVideoProcessor::GetFilterPropertyRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoProcessor.GetFilterPropertyRange
---

# IDirectXVideoProcessor::GetFilterPropertyRange


## -description

Retrieves the range of values for an image filter supported by this device.

## -parameters

### -param FilterSetting [in]

Filter setting to query. For more information, see <a href="/windows/desktop/medfound/dxva-image-filter-settings">DXVA Image Filter Settings</a>.

### -param pRange [out]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_valuerange">DXVA2_ValueRange</a> structure that receives the range of values for the setting specified in <i>FilterSetting</i>.

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
</table>

## -see-also

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor">IDirectXVideoProcessor</a>