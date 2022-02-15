---
UID: NE:dxgi1_5.DXGI_HDR_METADATA_TYPE
title: DXGI_HDR_METADATA_TYPE (dxgi1_5.h)
description: Specifies the header metadata type.
helpviewer_keywords: ["DXGI_HDR_METADATA_TYPE","DXGI_HDR_METADATA_TYPE enumeration [DXGI]","DXGI_HDR_METADATA_TYPE_HDR10","DXGI_HDR_METADATA_TYPE_NONE","direct3ddxgi.dxgi_hdr_metadata_type","dxgi1_5/DXGI_HDR_METADATA_TYPE","dxgi1_5/DXGI_HDR_METADATA_TYPE_HDR10","dxgi1_5/DXGI_HDR_METADATA_TYPE_NONE"]
old-location: direct3ddxgi\dxgi_hdr_metadata_type.htm
tech.root: direct3ddxgi
ms.assetid: EFDFEB2E-8631-4BD6-ADA1-D415B70CCBCD
ms.date: 12/05/2018
ms.keywords: DXGI_HDR_METADATA_TYPE, DXGI_HDR_METADATA_TYPE enumeration [DXGI], DXGI_HDR_METADATA_TYPE_HDR10, DXGI_HDR_METADATA_TYPE_NONE, direct3ddxgi.dxgi_hdr_metadata_type, dxgi1_5/DXGI_HDR_METADATA_TYPE, dxgi1_5/DXGI_HDR_METADATA_TYPE_HDR10, dxgi1_5/DXGI_HDR_METADATA_TYPE_NONE
req.header: dxgi1_5.h
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
req.typenames: DXGI_HDR_METADATA_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_HDR_METADATA_TYPE
 - dxgi1_5/DXGI_HDR_METADATA_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_5.h
api_name:
 - DXGI_HDR_METADATA_TYPE
---

# DXGI_HDR_METADATA_TYPE enumeration


## -description

Specifies the header metadata type.

## -enum-fields

### -field DXGI_HDR_METADATA_TYPE_NONE:0

Indicates there is no header metadata.

### -field DXGI_HDR_METADATA_TYPE_HDR10:1

Indicates the header metadata is held by a  <a href="/windows/desktop/api/dxgi1_5/ns-dxgi1_5-dxgi_hdr_metadata_hdr10">DXGI_HDR_METADATA_HDR10</a> structure.

### -field DXGI_HDR_METADATA_TYPE_HDR10PLUS:2

## -remarks

This enum is used by the <a href="/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgiswapchain4-sethdrmetadata">SetHDRMetaData</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/dxgi-1-5-improvements">DXGI 1.5 Improvements</a>



<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
