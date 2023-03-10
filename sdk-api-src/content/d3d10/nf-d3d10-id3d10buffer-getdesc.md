---
UID: NF:d3d10.ID3D10Buffer.GetDesc
title: ID3D10Buffer::GetDesc (d3d10.h)
description: Get the properties of a buffer resource. (ID3D10Buffer.GetDesc)
helpviewer_keywords: ["43c98e35-c17e-73a5-5b4f-535b750660f1","GetDesc","GetDesc method [Direct3D 10]","GetDesc method [Direct3D 10]","ID3D10Buffer interface","ID3D10Buffer interface [Direct3D 10]","GetDesc method","ID3D10Buffer.GetDesc","ID3D10Buffer::GetDesc","d3d10/ID3D10Buffer::GetDesc","direct3d10.id3d10buffer_getdesc"]
old-location: direct3d10\id3d10buffer_getdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10buffer_getdesc.htm
ms.date: 12/05/2018
ms.keywords: 43c98e35-c17e-73a5-5b4f-535b750660f1, GetDesc, GetDesc method [Direct3D 10], GetDesc method [Direct3D 10],ID3D10Buffer interface, ID3D10Buffer interface [Direct3D 10],GetDesc method, ID3D10Buffer.GetDesc, ID3D10Buffer::GetDesc, d3d10/ID3D10Buffer::GetDesc, direct3d10.id3d10buffer_getdesc
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Buffer::GetDesc
 - d3d10/ID3D10Buffer::GetDesc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Buffer.GetDesc
---

# ID3D10Buffer::GetDesc


## -description

Get the properties of a buffer resource.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_buffer_desc">D3D10_BUFFER_DESC</a>*</b>

Pointer to a resource description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-cd3d10_buffer_desc">D3D10_BUFFER_DESC</a>) filled in by the method. This pointer cannot be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer Interface</a>
