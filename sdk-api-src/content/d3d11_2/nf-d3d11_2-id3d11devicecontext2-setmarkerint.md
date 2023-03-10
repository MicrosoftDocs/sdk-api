---
UID: NF:d3d11_2.ID3D11DeviceContext2.SetMarkerInt
title: ID3D11DeviceContext2::SetMarkerInt (d3d11_2.h)
description: Allows applications to annotate graphics commands.
helpviewer_keywords: ["ID3D11DeviceContext2 interface [Direct3D 11]","SetMarkerInt method","ID3D11DeviceContext2.SetMarkerInt","ID3D11DeviceContext2::SetMarkerInt","SetMarkerInt","SetMarkerInt method [Direct3D 11]","SetMarkerInt method [Direct3D 11]","ID3D11DeviceContext2 interface","d3d11_2/ID3D11DeviceContext2::SetMarkerInt","direct3d11.id3d11devicecontext2_setmarkerint"]
old-location: direct3d11\id3d11devicecontext2_setmarkerint.htm
tech.root: direct3d11
ms.assetid: bb814f16-ca58-46ad-88eb-1c67b17d0c86
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext2 interface [Direct3D 11],SetMarkerInt method, ID3D11DeviceContext2.SetMarkerInt, ID3D11DeviceContext2::SetMarkerInt, SetMarkerInt, SetMarkerInt method [Direct3D 11], SetMarkerInt method [Direct3D 11],ID3D11DeviceContext2 interface, d3d11_2/ID3D11DeviceContext2::SetMarkerInt, direct3d11.id3d11devicecontext2_setmarkerint
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: D3d11_2.idl
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
 - ID3D11DeviceContext2::SetMarkerInt
 - d3d11_2/ID3D11DeviceContext2::SetMarkerInt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_2.h
api_name:
 - ID3D11DeviceContext2.SetMarkerInt
---

# ID3D11DeviceContext2::SetMarkerInt


## -description

Allows applications to annotate graphics commands.

## -parameters

### -param pLabel [in]

An optional string that will be logged to <a href="/previous-versions/dotnet/netframework-3.0/ms751538(v=vs.85)">ETW</a> when ETW logging is active. If <b>‘#d’</b> appears in the string, it will be replaced by the value of the <i>Data</i> parameter similar to the way <b>printf</b> works.

### -param Data

A signed data value that will be logged to ETW when ETW logging is active.

## -remarks

<b>SetMarkerInt</b> allows applications to annotate graphics commands, in order to provide more context to what the GPU is executing. When ETW logging or a support tool is enabled, an additional marker is correlated between the CPU and GPU timelines. The <i>pLabel</i> and <i>Data</i> value are logged to ETW. When the appropriate ETW logging is not enabled, this method does nothing.

## -see-also

<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a>