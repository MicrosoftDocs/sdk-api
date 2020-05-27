---
UID: NF:d3d12.ID3D12Device5.RemoveDevice
title: ID3D12Device5::RemoveDevice
description: You can call **RemoveDevice** to indicate to the Direct3D 12 runtime that the GPU device encountered a problem, and can no longer be used.
helpviewer_keywords: ["ID3D12Device5::RemoveDevice"]
tech.root: direct3d12
ms.date: 10/30/2019
ms.keywords: ID3D12Device5::RemoveDevice
f1_keywords:
- d3d12/ID3D12Device5.RemoveDevice
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d12.dll
api_name:
- ID3D12Device5::RemoveDevice
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

You can call **RemoveDevice** to indicate to the Direct3D 12 runtime that the GPU device encountered a problem, and can no longer be used. Doing so will cause all devices' monitored fences to be signaled. Your application typically doesn't need to explicitly call **RemoveDevice**.

## -remarks

## -see-also
