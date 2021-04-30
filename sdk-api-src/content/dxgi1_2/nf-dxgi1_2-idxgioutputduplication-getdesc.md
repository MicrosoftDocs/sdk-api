---
UID: NF:dxgi1_2.IDXGIOutputDuplication.GetDesc
title: IDXGIOutputDuplication::GetDesc (dxgi1_2.h)
description: Retrieves a description of a duplicated output. This description specifies the dimensions of the surface that contains the desktop image.
helpviewer_keywords: ["GetDesc","GetDesc method [DXGI]","GetDesc method [DXGI]","IDXGIOutputDuplication interface","IDXGIOutputDuplication interface [DXGI]","GetDesc method","IDXGIOutputDuplication.GetDesc","IDXGIOutputDuplication::GetDesc","direct3ddxgi.idxgioutputduplication_getdesc","dxgi1_2/IDXGIOutputDuplication::GetDesc"]
old-location: direct3ddxgi\idxgioutputduplication_getdesc.htm
tech.root: direct3ddxgi
ms.assetid: 40D2CF38-1528-48A4-BC0C-5D8CC132D0CB
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGIOutputDuplication interface, IDXGIOutputDuplication interface [DXGI],GetDesc method, IDXGIOutputDuplication.GetDesc, IDXGIOutputDuplication::GetDesc, direct3ddxgi.idxgioutputduplication_getdesc, dxgi1_2/IDXGIOutputDuplication::GetDesc
req.header: dxgi1_2.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutputDuplication::GetDesc
 - dxgi1_2/IDXGIOutputDuplication::GetDesc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIOutputDuplication.GetDesc
---

# IDXGIOutputDuplication::GetDesc


## -description

Retrieves a description of a duplicated output. This description specifies the dimensions of the surface that contains the desktop image.

## -parameters

### -param pDesc [out]

A pointer to a <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_outdupl_desc">DXGI_OUTDUPL_DESC</a> structure that describes the duplicated output. This parameter must not be <b>NULL</b>.

## -remarks

After an application creates an <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> interface, it calls <b>GetDesc</b> to retrieve the dimensions of the surface that contains the desktop image. The format of the desktop image is always <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a>