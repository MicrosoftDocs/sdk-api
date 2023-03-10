---
UID: NF:d3d12.ID3D12ProtectedSession.GetStatusFence
title: ID3D12ProtectedSession::GetStatusFence (d3d12.h)
description: Retrieves the fence for the protected session. From the fence, you can retrieve the current uniqueness validity value (using ID3D12Fence::GetCompletedValue), and add monitors for changes to its value. This is a read-only fence.
helpviewer_keywords: ["GetStatusFence","GetStatusFence method","GetStatusFence method","ID3D12ProtectedSession interface","ID3D12ProtectedSession interface","GetStatusFence method","ID3D12ProtectedSession.GetStatusFence","ID3D12ProtectedSession::GetStatusFence","d3d12/ID3D12ProtectedSession::GetStatusFence","direct3d12.id3d12protectedsession_getstatusfence"]
old-location: direct3d12\id3d12protectedsession_getstatusfence.htm
tech.root: direct3d12
ms.assetid: A2B4A826-198C-4D6E-9006-B6470DE1121E
ms.date: 12/05/2018
ms.keywords: GetStatusFence, GetStatusFence method, GetStatusFence method,ID3D12ProtectedSession interface, ID3D12ProtectedSession interface,GetStatusFence method, ID3D12ProtectedSession.GetStatusFence, ID3D12ProtectedSession::GetStatusFence, d3d12/ID3D12ProtectedSession::GetStatusFence, direct3d12.id3d12protectedsession_getstatusfence
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
 - ID3D12ProtectedSession::GetStatusFence
 - d3d12/ID3D12ProtectedSession::GetStatusFence
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
 - ID3D12ProtectedSession.GetStatusFence
---

# ID3D12ProtectedSession::GetStatusFence


## -description

Retrieves the fence for the protected session. From the fence, you can retrieve the current uniqueness validity value (using <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue">ID3D12Fence::GetCompletedValue</a>), and add monitors for changes to its value. This is a read-only fence.

## -parameters

### -param riid

The GUID of the interface to a fence. Most commonly, <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>, although it may be any GUID for any interface. If the protected session object doesn’t support the interface for this GUID, the function returns <b>E_NOINTERFACE</b>.

### -param ppFence [optional]

A pointer to a memory block that receives a pointer to the fence for the given protected session.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12protectedsession">ID3D12ProtectedSession</a>