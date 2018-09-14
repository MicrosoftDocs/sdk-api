---
UID: NE:d3d11.D3D11_COUNTER
title: D3D11_COUNTER
author: windows-sdk-content
description: Options for performance counters.
old-location: direct3d11\d3d11_counter.htm
tech.root: direct3d11
ms.assetid: b6a5cc7e-48e5-478a-aa9c-8b2878c0de6b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 2fda44d5-455a-a992-9f44-d95b5d7f369f, D3D11_COUNTER, D3D11_COUNTER enumeration [Direct3D 11], D3D11_COUNTER_DEVICE_DEPENDENT_0, d3d11/D3D11_COUNTER, d3d11/D3D11_COUNTER_DEVICE_DEPENDENT_0, direct3d11.d3d11_counter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_COUNTER
product: Windows
targetos: Windows
req.typenames: D3D11_COUNTER
req.redist: 
---

# D3D11_COUNTER enumeration


## -description


Options for performance counters.


## -enum-fields




### -field D3D11_COUNTER_DEVICE_DEPENDENT_0

Define a performance counter that is dependent on the hardware device.


## -remarks



Independent hardware vendors may define their own set of performance counters for their devices, by giving the enumeration value a number that is greater than the value for D3D11_COUNTER_DEVICE_DEPENDENT_0.

This enumeration is used by <a href="https://msdn.microsoft.com/a0816409-fbe1-4b45-9b69-6f85b20008cb">D3D11_COUNTER_DESC</a> and <a href="https://msdn.microsoft.com/64730e19-1a9e-4494-a3aa-314fd72281e1">D3D11_COUNTER_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

