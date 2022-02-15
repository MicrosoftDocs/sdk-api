---
UID: NN:d3d12.ID3D12SDKConfiguration
title: ID3D12SDKConfiguration
description: Provides SDK configuration methods.
tech.root: direct3d12
ms.date: 08/25/2021
req.construct-type: iface
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
f1_keywords:
 - ID3D12SDKConfiguration
 - d3d12/ID3D12SDKConfiguration
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
 - ID3D12SDKConfiguration
---

## -description

Provides SDK configuration methods. A pointer to this interface can be retrieved by calling the [D3D12GetInterface](nf-d3d12-d3d12getinterface.md) free function with the **CLSID_D3D12SDKConfiguration** CLSID.

## -remarks

Tools that play back API capture such as PIX, and test harnesses such as the HLK, require modification to support the redist. Such tools can choose to ship with the latest redist. Direct3D's API compatibility through updates should mean that an API capture tool can capture on an older version of the Direct3D 12 SDK, and play it back on the newer version. However, some scenarios require more flexibility in selecting the SDK version.

## -see-also
