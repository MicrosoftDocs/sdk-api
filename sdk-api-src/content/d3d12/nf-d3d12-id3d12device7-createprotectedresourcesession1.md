---
UID: NF:d3d12.ID3D12Device7.CreateProtectedResourceSession1
title: ID3D12Device7::CreateProtectedResourceSession1
description: Revises the [**ID3D12Device4::CreateProtectedResourceSession**](../d3d12/nf-d3d12-id3d12device4-createprotectedresourcesession.md) method with provision **GUID** that indicates the type of protected resource session.
helpviewer_keywords: ["ID3D12Device7 interface","CreateProtectedResourceSession1 method","ID3D12Device7.CreateProtectedResourceSession1","ID3D12Device7::CreateProtectedResourceSession1","CreateProtectedResourceSession1","CreateProtectedResourceSession1 method","CreateProtectedResourceSession1 method","ID3D12Device7 interface","direct3d12.id3d12device7_createprotectedresourcesssion1","d3d12/ID3D12Device7::CreateProtectedResourceSession1"]
tech.root: direct3d12
ms.date: 09/15/2020
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: d3d12.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device7::CreateProtectedResourceSession1
f1_keywords:
 - d3d12/ID3D12Device7::CreateProtectedResourceSession1
dev_langs:
 - c++
---

## -description

**CreateProtectedResourceSession1** revises the [**ID3D12Device4::CreateProtectedResourceSession**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createprotectedresourcesession) method with provision (in the structure passed via the *pDesc* parameter) for a globally unique identifier (**GUID**) that indicates the type of protected resource session.

Calling **ID3D12Device4::CreateProtectedResourceSession** is equivalent to calling **ID3D12Device7::CreateProtectedResourceSession1** with the **D3D12_PROTECTED_RESOURCES_SESSION_HARDWARE_PROTECTED** GUID.

## -parameters

### -param pDesc

Type: \_In\_ **const [D3D12_PROTECTED_RESOURCE_SESSION_DESC1](./ns-d3d12-d3d12_protected_resource_session_desc1.md)\***

A pointer to a constant **D3D12_PROTECTED_RESOURCE_SESSION_DESC1** structure, describing the session to create.

### -param riid

Type: \_In\_ **REFIID**

The GUID of the interface to a protected session. Most commonly, [ID3D12ProtectedResourceSession1](./nn-d3d12-id3d12protectedresourcesession1.md), although it may be any **GUID** for any interface. If the protected session object doesn't support the interface for this **GUID**, the getter will return **E_NOINTERFACE**.

### -param ppSession

Type: \_COM\_Outptr\_ **void\*\***

A pointer to a memory block that receives a pointer to the session for the given protected session (the specific interface type returned depends on *riid*).

## -returns

## -remarks

## -see-also
