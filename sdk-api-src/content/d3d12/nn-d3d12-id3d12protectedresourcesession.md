---
UID: NN:d3d12.ID3D12ProtectedResourceSession
title: ID3D12ProtectedResourceSession (d3d12.h)
author: windows-sdk-content
description: Monitors the validity of a protected resource session.
old-location: direct3d12\id3d12protectedresourcesession.htm
tech.root: direct3d12
ms.assetid: 9D4833DB-DF9E-46A8-9EF7-667A95F3EFDD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12ProtectedResourceSession, ID3D12ProtectedResourceSession interface, ID3D12ProtectedResourceSession interface,described, d3d12/ID3D12ProtectedResourceSession, direct3d12.id3d12protectedresourcesession
ms.topic: interface
f1_keywords: 
 - "d3d12/ID3D12ProtectedResourceSession"
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12ProtectedResourceSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12ProtectedResourceSession interface

## -description

Monitors the validity of a protected resource session. This interface extends [ID3D12ProtectedSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedsession).

You can obtain an **ID3D12ProtectedResourceSession** by calling [ID3D12Device4::CreateProtectedResourceSession](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createprotectedresourcesession).

## -see-also

<a href="https://docs.microsoft.com/en-us/windows/desktop/api/d3d12/nn-d3d12-id3d12protectedsession">ID3D12ProtectedSession</a>