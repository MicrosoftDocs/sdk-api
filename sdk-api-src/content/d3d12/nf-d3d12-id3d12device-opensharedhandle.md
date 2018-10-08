---
UID: NF:d3d12.ID3D12Device.OpenSharedHandle
title: ID3D12Device::OpenSharedHandle
author: windows-sdk-content
description: Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.
old-location: direct3d12\id3d12device_opensharedhandle.htm
tech.root: direct3d12
ms.assetid: 4F428B06-2906-4ED6-BB75-5DACF2155FA9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID3D12Device interface,OpenSharedHandle method, ID3D12Device.OpenSharedHandle, ID3D12Device::OpenSharedHandle, OpenSharedHandle, OpenSharedHandle method, OpenSharedHandle method,ID3D12Device interface, d3d12/ID3D12Device::OpenSharedHandle, direct3d12.id3d12device_opensharedhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D12Device.OpenSharedHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::OpenSharedHandle


## -description


Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID.
        


## -parameters




### -param NTHandle [in]

Type: <b>HANDLE</b>

The handle that was output by the call to 
            <a href="https://msdn.microsoft.com/en-us/library/Dn899183(v=VS.85).aspx">ID3D12Device::CreateSharedHandle</a>.
          


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for one of the following interfaces:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788687(v=VS.85).aspx">ID3D12Heap</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn899188(v=VS.85).aspx">ID3D12Fence</a>
</li>
</ul>
The <b>REFIID</b>, or <b>GUID</b>, of the interface can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12Heap) will get the <b>GUID</b> of the interface to a resource.
          


### -param ppvObj [out, optional]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to one of the following interfaces:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788687(v=VS.85).aspx">ID3D12Heap</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn899188(v=VS.85).aspx">ID3D12Fence</a>
</li>
</ul>

## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn788650(v=VS.85).aspx">ID3D12Device</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn933253(v=VS.85).aspx">Multi-Adapter</a>
 

 

