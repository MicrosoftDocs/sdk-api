---
UID: NF:mfapi.MFMapDXGIFormatToDX9Format
title: MFMapDXGIFormatToDX9Format function (mfapi.h)
description: Converts a Microsoft DirectX Graphics Infrastructure (DXGI) format identifier to a Microsoft Direct3D 9 format identifier.
helpviewer_keywords: ["MFMapDXGIFormatToDX9Format","MFMapDXGIFormatToDX9Format function [Media Foundation]","mf.mfmapdxgiformattodx9format","mfapi/MFMapDXGIFormatToDX9Format"]
old-location: mf\mfmapdxgiformattodx9format.htm
tech.root: mf
ms.assetid: D3DF4739-31CC-4D0E-9EF2-6FCCAB8969EF
ms.date: 12/05/2018
ms.keywords: MFMapDXGIFormatToDX9Format, MFMapDXGIFormatToDX9Format function [Media Foundation], mf.mfmapdxgiformattodx9format, mfapi/MFMapDXGIFormatToDX9Format
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
 - MFMapDXGIFormatToDX9Format
 - mfapi/MFMapDXGIFormatToDX9Format
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
 - MFMapDXGIFormatToDX9Format
---

# MFMapDXGIFormatToDX9Format function


## -description

Converts a Microsoft DirectX Graphics Infrastructure (DXGI) format identifier to a Microsoft Direct3D 9 format identifier.

## -parameters

### -param dx11 [in]

The <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> value to convert.

## -returns

Returns a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_d3dformat_data">D3DFORMAT</a> value or FOURCC code.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfmapdx9formattodxgiformat">MFMapDX9FormatToDXGIFormat</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>