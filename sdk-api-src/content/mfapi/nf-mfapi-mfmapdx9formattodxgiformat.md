---
UID: NF:mfapi.MFMapDX9FormatToDXGIFormat
title: MFMapDX9FormatToDXGIFormat function (mfapi.h)
description: Converts a Microsoft Direct3D 9 format identifier to a Microsoft DirectX Graphics Infrastructure (DXGI) format identifier.
helpviewer_keywords: ["MFMapDX9FormatToDXGIFormat","MFMapDX9FormatToDXGIFormat function [Media Foundation]","mf.mfmapdx9formattodxgiformat","mfapi/MFMapDX9FormatToDXGIFormat"]
old-location: mf\mfmapdx9formattodxgiformat.htm
tech.root: mf
ms.assetid: 66B6A512-0371-4984-88B3-CB37BE52AEC5
ms.date: 12/05/2018
ms.keywords: MFMapDX9FormatToDXGIFormat, MFMapDX9FormatToDXGIFormat function [Media Foundation], mf.mfmapdx9formattodxgiformat, mfapi/MFMapDX9FormatToDXGIFormat
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFMapDX9FormatToDXGIFormat
 - mfapi/MFMapDX9FormatToDXGIFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFMapDX9FormatToDXGIFormat
---

# MFMapDX9FormatToDXGIFormat function


## -description

Converts a Microsoft Direct3D 9 format identifier to a Microsoft DirectX Graphics Infrastructure (DXGI) format identifier.

## -parameters

### -param dx9 [in]

The <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_d3dformat_data">D3DFORMAT</a> value or FOURCC code to convert.

## -returns

Returns a <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> value.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfmapdxgiformattodx9format">MFMapDXGIFormatToDX9Format</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>