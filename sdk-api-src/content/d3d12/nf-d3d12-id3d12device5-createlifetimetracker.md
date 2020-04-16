---
UID: NF:d3d12.ID3D12Device5.CreateLifetimeTracker
title: ID3D12Device5::CreateLifetimeTracker
description: Creates a lifetime tracker associated with an application-defined callback; the callback receives notifications when the lifetime of a tracked object is changed.helpviewer_keywords: ["ID3D12Device5::CreateLifetimeTracker"]
tech.root: direct3d12
ms.date: 10/30/2019
ms.keywords: ID3D12Device5::CreateLifetimeTracker
f1_keywords:
- d3d12/ID3D12Device5.CreateLifetimeTracker
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
- ID3D12Device5::CreateLifetimeTracker
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Creates a lifetime tracker associated with an application-defined callback; the callback receives notifications when the lifetime of a tracked object is changed.

## -parameters

### -param pOwner [in]

Type: **[ID3D12LifetimeOwner](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner)\***

A pointer to an **ID3D12LifetimeOwner** interface representing the application-defined callback.

### -param riid [in]

Type: **REFIID**

A reference to the interface identifier (IID) of the interface to return in *ppvTracker*.

### -param ppvTracker [out]

Type: **void\*\***

A pointer to a memory block that receives the requested interface pointer to the created object.

## -returns

## -remarks

## -see-also
