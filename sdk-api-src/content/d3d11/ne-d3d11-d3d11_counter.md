---
UID: NE:d3d11.D3D11_COUNTER
title: D3D11_COUNTER (d3d11.h)
description: Options for performance counters.
helpviewer_keywords: ["2fda44d5-455a-a992-9f44-d95b5d7f369f","D3D11_COUNTER","D3D11_COUNTER enumeration [Direct3D 11]","D3D11_COUNTER_DEVICE_DEPENDENT_0","d3d11/D3D11_COUNTER","d3d11/D3D11_COUNTER_DEVICE_DEPENDENT_0","direct3d11.d3d11_counter"]
old-location: direct3d11\d3d11_counter.htm
tech.root: direct3d11
ms.assetid: b6a5cc7e-48e5-478a-aa9c-8b2878c0de6b
ms.date: 12/05/2018
ms.keywords: 2fda44d5-455a-a992-9f44-d95b5d7f369f, D3D11_COUNTER, D3D11_COUNTER enumeration [Direct3D 11], D3D11_COUNTER_DEVICE_DEPENDENT_0, d3d11/D3D11_COUNTER, d3d11/D3D11_COUNTER_DEVICE_DEPENDENT_0, direct3d11.d3d11_counter
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_COUNTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_COUNTER
 - d3d11/D3D11_COUNTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_COUNTER
---

# D3D11_COUNTER enumeration


## -description

Options for performance counters.

## -enum-fields

### -field D3D11_COUNTER_DEVICE_DEPENDENT_0:0x40000000

Define a performance counter that is dependent on the hardware device.

## -remarks

Independent hardware vendors may define their own set of performance counters for their devices, by giving the enumeration value a number that is greater than the value for D3D11_COUNTER_DEVICE_DEPENDENT_0.

This enumeration is used by <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_counter_desc">D3D11_COUNTER_DESC</a> and <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_counter_info">D3D11_COUNTER_INFO</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
