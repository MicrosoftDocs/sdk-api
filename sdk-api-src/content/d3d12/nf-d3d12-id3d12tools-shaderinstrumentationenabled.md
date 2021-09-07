---
UID: NF:d3d12.ID3D12Tools.ShaderInstrumentationEnabled
title: ID3D12Tools::ShaderInstrumentationEnabled (d3d12.h)
description: Determines whether shader instrumentation is enabled.
helpviewer_keywords: ["ID3D12Tools interface","ShaderInstrumentationEnabled method","ID3D12Tools.ShaderInstrumentationEnabled","ID3D12Tools::ShaderInstrumentationEnabled","ShaderInstrumentationEnabled","ShaderInstrumentationEnabled method","ShaderInstrumentationEnabled method","ID3D12Tools interface","d3d12/ID3D12Tools::ShaderInstrumentationEnabled","direct3d12.id3d12tools_shaderinstrumentationenabled"]
old-location: direct3d12\id3d12tools_shaderinstrumentationenabled.htm
tech.root: direct3d12
ms.assetid: 02A36358-5015-4CA1-B329-CCF074CF8F40
ms.date: 12/05/2018
ms.keywords: ID3D12Tools interface,ShaderInstrumentationEnabled method, ID3D12Tools.ShaderInstrumentationEnabled, ID3D12Tools::ShaderInstrumentationEnabled, ShaderInstrumentationEnabled, ShaderInstrumentationEnabled method, ShaderInstrumentationEnabled method,ID3D12Tools interface, d3d12/ID3D12Tools::ShaderInstrumentationEnabled, direct3d12.id3d12tools_shaderinstrumentationenabled
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Tools::ShaderInstrumentationEnabled
 - d3d12/ID3D12Tools::ShaderInstrumentationEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Tools.ShaderInstrumentationEnabled
---

# ID3D12Tools::ShaderInstrumentationEnabled


## -description

Determines whether shader instrumentation is enabled.



## -returns

Type: <b>BOOL</b>

Returns TRUE if shader instrumentation is enabled; otherwise FALSE.

## -remarks

Do not use this interface in your application, it's not intended or supported for any scenario other than to enable tooling such as PIX.

Developer Mode must be enabled for this interface to respond.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12tools">ID3D12Tools</a>
