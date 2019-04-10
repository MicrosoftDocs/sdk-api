---
UID: NF:d3d12.ID3D12ProtectedSession.GetStatusFence
title: ID3D12ProtectedSession::GetStatusFence (d3d12.h)
author: windows-sdk-content
description: Retrieves the fence for the protected session. From the fence, you can retrieve the current uniqueness validity value (using ID3D12Fence::GetCompletedValue), and add monitors for changes to its value. This is a read-only fence.
old-location: direct3d12\id3d12protectedsession_getstatusfence.htm
tech.root: direct3d12
ms.assetid: A2B4A826-198C-4D6E-9006-B6470DE1121E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStatusFence, GetStatusFence method, GetStatusFence method,ID3D12ProtectedSession interface, ID3D12ProtectedSession interface,GetStatusFence method, ID3D12ProtectedSession.GetStatusFence, ID3D12ProtectedSession::GetStatusFence, d3d12/ID3D12ProtectedSession::GetStatusFence, direct3d12.id3d12protectedsession_getstatusfence
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12ProtectedSession.GetStatusFence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12ProtectedSession::GetStatusFence


## -description


Retrieves the fence for the protected session. From the fence, you can retrieve the current uniqueness validity value (using <a href="https://msdn.microsoft.com/2F2DDFC5-8D31-4BCE-B378-610C95D7805F">ID3D12Fence::GetCompletedValue</a>), and add monitors for changes to its value. This is a read-only fence.


## -parameters




### -param riid

The GUID of the interface to a fence. Most commonly, <a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>, although it may be any GUID for any interface. If the protected session object doesn’t support the interface for this GUID, the function returns <b>E_NOINTERFACE</b>.


### -param ppFence [optional]

A pointer to a memory block that receives a pointer to the fence for the given protected session.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BBB87F18-A4F4-44E7-AFD8-803BD2C7C753">ID3D12ProtectedSession</a>
 

 

