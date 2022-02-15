---
UID: NF:d3d12.ID3D12Tools.EnableShaderInstrumentation
title: ID3D12Tools::EnableShaderInstrumentation (d3d12.h)
description: This method enables tools such as PIX to instrument shaders.
helpviewer_keywords: ["EnableShaderInstrumentation","EnableShaderInstrumentation method","EnableShaderInstrumentation method","ID3D12Tools interface","ID3D12Tools interface","EnableShaderInstrumentation method","ID3D12Tools.EnableShaderInstrumentation","ID3D12Tools::EnableShaderInstrumentation","d3d12/ID3D12Tools::EnableShaderInstrumentation","direct3d12.id3d12tools_enableshaderinstrumentation"]
old-location: direct3d12\id3d12tools_enableshaderinstrumentation.htm
tech.root: direct3d12
ms.assetid: 35920253-1153-42AD-AEAC-2C646FF15879
ms.date: 12/05/2018
ms.keywords: EnableShaderInstrumentation, EnableShaderInstrumentation method, EnableShaderInstrumentation method,ID3D12Tools interface, ID3D12Tools interface,EnableShaderInstrumentation method, ID3D12Tools.EnableShaderInstrumentation, ID3D12Tools::EnableShaderInstrumentation, d3d12/ID3D12Tools::EnableShaderInstrumentation, direct3d12.id3d12tools_enableshaderinstrumentation
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
 - ID3D12Tools::EnableShaderInstrumentation
 - d3d12/ID3D12Tools::EnableShaderInstrumentation
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
 - ID3D12Tools.EnableShaderInstrumentation
---

# ID3D12Tools::EnableShaderInstrumentation


## -description

This method enables tools such as PIX to instrument shaders.

## -parameters

### -param bEnable

Type: <b>BOOL</b>

TRUE to enable shader instrumentation; otherwise, FALSE.

## -remarks

Do not use this interface in your application, it's not intended or supported for any scenario other than to enable tooling such as PIX.

Developer Mode must be enabled for this interface to respond.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12tools">ID3D12Tools</a>