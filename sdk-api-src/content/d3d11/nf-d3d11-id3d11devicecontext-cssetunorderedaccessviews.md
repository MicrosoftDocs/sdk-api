---
UID: NF:d3d11.ID3D11DeviceContext.CSSetUnorderedAccessViews
title: ID3D11DeviceContext::CSSetUnorderedAccessViews (d3d11.h)
description: Sets an array of views for an unordered resource.
helpviewer_keywords: ["16820cec-2cc5-1d17-4d7f-118d1fd9660b","CSSetUnorderedAccessViews","CSSetUnorderedAccessViews method [Direct3D 11]","CSSetUnorderedAccessViews method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CSSetUnorderedAccessViews method","ID3D11DeviceContext.CSSetUnorderedAccessViews","ID3D11DeviceContext::CSSetUnorderedAccessViews","d3d11/ID3D11DeviceContext::CSSetUnorderedAccessViews","direct3d11.id3d11devicecontext_cssetunorderedaccessviews"]
old-location: direct3d11\id3d11devicecontext_cssetunorderedaccessviews.htm
tech.root: direct3d11
ms.assetid: 384a15c0-a035-4f83-a927-e2f763e5fb44
ms.date: 12/05/2018
ms.keywords: 16820cec-2cc5-1d17-4d7f-118d1fd9660b, CSSetUnorderedAccessViews, CSSetUnorderedAccessViews method [Direct3D 11], CSSetUnorderedAccessViews method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSSetUnorderedAccessViews method, ID3D11DeviceContext.CSSetUnorderedAccessViews, ID3D11DeviceContext::CSSetUnorderedAccessViews, d3d11/ID3D11DeviceContext::CSSetUnorderedAccessViews, direct3d11.id3d11devicecontext_cssetunorderedaccessviews
req.header: d3d11.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::CSSetUnorderedAccessViews
 - d3d11/ID3D11DeviceContext::CSSetUnorderedAccessViews
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.CSSetUnorderedAccessViews
---

# ID3D11DeviceContext::CSSetUnorderedAccessViews


## -description

Sets an array of views for an unordered resource.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first element in the zero-based array to begin setting  (ranges from 0 to D3D11_1_UAV_SLOT_COUNT - 1). D3D11_1_UAV_SLOT_COUNT is defined as 64.

### -param NumUAVs [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of views to set (ranges from 0 to D3D11_1_UAV_SLOT_COUNT - <i>StartSlot</i>).

### -param ppUnorderedAccessViews [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> pointers to be set by the method.

### -param pUAVInitialCounts [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of append and consume buffer offsets. A value of -1 indicates to keep the current offset. Any other values set the hidden counter
            for that appendable and consumable UAV. <i>pUAVInitialCounts</i> is only relevant for UAVs that were created with either
            <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag">D3D11_BUFFER_UAV_FLAG_APPEND</a> or <b>D3D11_BUFFER_UAV_FLAG_COUNTER</b> specified
            when the UAV was created; otherwise, the argument is ignored.

## -remarks

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>