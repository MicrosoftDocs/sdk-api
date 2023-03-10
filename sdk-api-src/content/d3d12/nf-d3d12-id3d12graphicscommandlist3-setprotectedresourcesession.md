---
UID: NF:d3d12.ID3D12GraphicsCommandList3.SetProtectedResourceSession
title: ID3D12GraphicsCommandList3::SetProtectedResourceSession
description: Specifies whether or not protected resources can be accessed by subsequent commands in the command list.
helpviewer_keywords: ["ID3D12GraphicsCommandList3 interface","SetProtectedResourceSession method","ID3D12GraphicsCommandList3.SetProtectedResourceSession","ID3D12GraphicsCommandList3::SetProtectedResourceSession","SetProtectedResourceSession","SetProtectedResourceSession method","SetProtectedResourceSession method","ID3D12GraphicsCommandList3 interface","d3d12/ID3D12GraphicsCommandList3::SetProtectedResourceSession","direct3d12.id3d12graphicscommandlist3_setprotectedresourcesession"]
old-location: direct3d12\id3d12graphicscommandlist3_setprotectedresourcesession.htm
tech.root: direct3d12
ms.assetid: 5D176919-34DC-4FD5-A577-78B03D5AB76B
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList3 interface,SetProtectedResourceSession method, ID3D12GraphicsCommandList3.SetProtectedResourceSession, ID3D12GraphicsCommandList3::SetProtectedResourceSession, SetProtectedResourceSession, SetProtectedResourceSession method, SetProtectedResourceSession method,ID3D12GraphicsCommandList3 interface, d3d12/ID3D12GraphicsCommandList3::SetProtectedResourceSession, direct3d12.id3d12graphicscommandlist3_setprotectedresourcesession
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D12GraphicsCommandList3::SetProtectedResourceSession
 - d3d12/ID3D12GraphicsCommandList3::SetProtectedResourceSession
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
 - ID3D12GraphicsCommandList3.SetProtectedResourceSession
---

## -description

Specifies whether or not protected resources can be accessed by subsequent commands in the command list. By default, no protected resources are enabled. After calling <b>SetProtectedResourceSession</b> with a valid session, protected resources of the same type can refer to that session. After calling <b>SetProtectedResourceSession</b> with <b>NULL</b>, no protected resources can be accessed.

## -parameters

### -param pProtectedResourceSession [in, optional]

Type: **[ID3D12ProtectedResourceSession](./nn-d3d12-id3d12protectedresourcesession.md)\***

An optional pointer to an **ID3D12ProtectedResourceSession**. You can obtain an **ID3D12ProtectedResourceSession** by calling [ID3D12Device4::CreateProtectedResourceSession](./nf-d3d12-id3d12device4-createprotectedresourcesession.md).

## -returns

If set, indicates that protected resources can be accessed with the given session. Access to protected resources can only happen after <b>SetProtectedResourceSession</b> is called with a valid session. The command list state is cleared when calling this method. If you pass <b>NULL</b>, then no protected resources can be accessed.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist3">ID3D12GraphicsCommandList3</a>