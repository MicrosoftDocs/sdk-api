---
UID: NF:d3d12.ID3D12Device4.CreateProtectedResourceSession
title: ID3D12Device4::CreateProtectedResourceSession
description: Creates an object that represents a session for content protection.
helpviewer_keywords: ["ID3D12Device4 interface","CreateProtectedResourceSession method","ID3D12Device4.CreateProtectedResourceSession","ID3D12Device4::CreateProtectedResourceSession","CreateProtectedResourceSession","CreateProtectedResourceSession method","CreateProtectedResourceSession method","ID3D12Device4 interface","direct3d12.id3d12device4_createprotectedresourcesession","d3d12/ID3D12Device4::CreateProtectedResourceSession"]
tech.root: direct3d12
ms.date: 10/15/2019
ms.keywords: ID3D12Device4 interface,CreateProtectedResourceSession method, ID3D12Device4.CreateProtectedResourceSession, ID3D12Device4::CreateProtectedResourceSession, CreateProtectedResourceSession, CreateProtectedResourceSession method, CreateProtectedResourceSession method,ID3D12Device4 interface, direct3d12.id3d12device4_createprotectedresourcesession, d3d12/ID3D12Device4::CreateProtectedResourceSession
req.construct-type: function
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
req.lib: d3d12.lib
req.dll: d3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - ID3D12Device4::CreateProtectedResourceSession
 - d3d12/ID3D12Device4::CreateProtectedResourceSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device4::CreateProtectedResourceSession
---

## -description

Creates an object that represents a session for content protection. You can then provide that session when you're creating resource or heap objects, to indicate that they should be protected.

> [!NOTE]
> Memory contents can't be transferred from a protected resource to an unprotected resource.

## -parameters

### -param pDesc [in]

Type: **const [D3D12_PROTECTED_RESOURCE_SESSION_DESC](./ns-d3d12-d3d12_protected_resource_session_desc.md)\***

A pointer to a constant **D3D12_PROTECTED_RESOURCE_SESSION_DESC** structure, describing the session to create.

### -param riid [in]

Type: **REFIID**

A reference to the globally unique identifier (**GUID**) of the [ID3D12ProtectedResourceSession](./nn-d3d12-id3d12protectedresourcesession.md) interface.

### -param ppSession [out]

Type: **void\*\***

A pointer to a memory block that receives an [ID3D12ProtectedResourceSession](./nn-d3d12-id3d12protectedresourcesession.md) interface pointer to the created session object.

## -returns

## -remarks

## -see-also
