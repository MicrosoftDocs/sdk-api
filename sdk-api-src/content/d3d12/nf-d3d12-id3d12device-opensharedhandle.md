---
UID: NF:d3d12.ID3D12Device.OpenSharedHandle
title: ID3D12Device::OpenSharedHandle
author: windows-sdk-content
description: Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.
old-location: direct3d12\id3d12device_opensharedhandle.htm
old-project: direct3d12
ms.assetid: 4F428B06-2906-4ED6-BB75-5DACF2155FA9
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12Device interface,OpenSharedHandle method, ID3D12Device.OpenSharedHandle, ID3D12Device::OpenSharedHandle, OpenSharedHandle, OpenSharedHandle method, OpenSharedHandle method,ID3D12Device interface, d3d12/ID3D12Device::OpenSharedHandle, direct3d12.id3d12device_opensharedhandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.OpenSharedHandle
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::OpenSharedHandle


## -description


Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.
        


## -parameters




### -param NTHandle [in]

Type: <b>HANDLE</b>

The handle that was output by the call to 
            <a href="https://msdn.microsoft.com/AFF058FF-358F-4FF3-8C92-57A9D34B27D9">ID3D12Device::CreateSharedHandle</a>.
          


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for one of the following interfaces:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/3791C64F-76D7-4580-A444-F2CEA3EB10CE">ID3D12Heap</a>
</li>
<li>
<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>
</li>
</ul>
The <b>REFIID</b>, or <b>GUID</b>, of the interface can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12Heap) will get the <b>GUID</b> of the interface to a resource.
          


### -param ppvObj [out, optional]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to one of the following interfaces:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/3791C64F-76D7-4580-A444-F2CEA3EB10CE">ID3D12Heap</a>
</li>
<li>
<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>
</li>
</ul>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>
 

 

