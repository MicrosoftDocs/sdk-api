---
UID: NE:d3d12.D3D12_PREDICATION_OP
title: D3D12_PREDICATION_OP
author: windows-sdk-content
description: Specifies the predication operation to apply.
old-location: direct3d12\d3d12_predication_op.htm
old-project: direct3d12
ms.assetid: 2A650FE4-7D24-4852-9435-7C3CB73848AB
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_PREDICATION_OP, D3D12_PREDICATION_OP enumeration, D3D12_PREDICATION_OP_EQUAL_ZERO, D3D12_PREDICATION_OP_NOT_EQUAL_ZERO, d3d12/D3D12_PREDICATION_OP, d3d12/D3D12_PREDICATION_OP_EQUAL_ZERO, d3d12/D3D12_PREDICATION_OP_NOT_EQUAL_ZERO, direct3d12.d3d12_predication_op
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D12_PREDICATION_OP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_PREDICATION_OP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_PREDICATION_OP enumeration


## -description


Specifies the predication operation to apply.
        


## -enum-fields




### -field D3D12_PREDICATION_OP_EQUAL_ZERO

Enables predication if all 64-bits are zero.
          


### -field D3D12_PREDICATION_OP_NOT_EQUAL_ZERO

Enables predication if at least one of the 64-bits are not zero.
          


## -remarks



This enum is used by <a href="https://msdn.microsoft.com/21526012-A675-40E8-A11C-4CBA5C12B9CF">SetPredication</a>.
        

Predication is decoupled from queries.
          Predication can be set based on the value of 64-bits within a buffer.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/5C5138C7-F6E8-4646-961A-0E2312B5356B">Predication</a>
 

 

