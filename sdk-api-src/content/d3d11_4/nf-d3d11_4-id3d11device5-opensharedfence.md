---
UID: NF:d3d11_4.ID3D11Device5.OpenSharedFence
title: ID3D11Device5::OpenSharedFence
author: windows-sdk-content
description: Opens a handle for a shared fence by using HANDLE and REFIID.
old-location: direct3d11\id3d11device5_opensharedfence.htm
tech.root: direct3d11
ms.assetid: 3EB1BA51-61CB-4389-84A9-77DAC9815AC7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11Device5 interface [Direct3D 11],OpenSharedFence method, ID3D11Device5.OpenSharedFence, ID3D11Device5::OpenSharedFence, OpenSharedFence, OpenSharedFence method [Direct3D 11], OpenSharedFence method [Direct3D 11],ID3D11Device5 interface, d3d11_4/ID3D11Device5::OpenSharedFence, direct3d11.id3d11device5_opensharedfence
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_4.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device5.OpenSharedFence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device5::OpenSharedFence


## -description


Opens a handle for a shared fence by using HANDLE and REFIID.

This member function is a limited version of the Direct3D 12 <a href="https://msdn.microsoft.com/4F428B06-2906-4ED6-BB75-5DACF2155FA9">ID3D12Device::OpenSharedHandle</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios. Unlike <b>ID3D12Device::OpenSharedHandle</b> which operates on resources, heaps, and fences, the <b>ID3D11Device5::OpenSharedFence</b> function only operates on fences; in Direct3D 11, shared resources are opened with the <a href="direct3d11.id3d11device_opensharedresource1">ID3D11Device::OpenSharedResource1</a> member function.


## -parameters




### -param hFence [in]

Type: <b>HANDLE</b>

The handle that was returned by a call to <a href="https://msdn.microsoft.com/07447C9A-8F69-4FCA-B75C-D7015292F25D">ID3D11Fence::CreateSharedHandle</a> or <a href="https://msdn.microsoft.com/AFF058FF-358F-4FF3-8C92-57A9D34B27D9">ID3D12Device::CreateSharedHandle</a>.
          


### -param ReturnedInterface

TBD


### -param ppFence [out, optional]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C">ID3D11Fence</a> interface.
          


#### - Returned Interface

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the <a href="https://msdn.microsoft.com/DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C">ID3D11Fence</a> interface. The <b>REFIID</b>, or <b>GUID</b>, of the interface can be obtained by using the __uuidof() macro. For example, __uuidof(ID3D11Fence) will get the <b>GUID</b> of the interface to the fence.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/C077BAD4-08D2-4F1F-8313-5066F68F014C">ID3D11Device5</a>



<a href="direct3d12.multi-engine">Multi-Adapter (Direct3D 12)</a>
 

 

