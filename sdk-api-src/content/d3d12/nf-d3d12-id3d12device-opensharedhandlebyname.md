---
UID: NF:d3d12.ID3D12Device.OpenSharedHandleByName
title: ID3D12Device::OpenSharedHandleByName (d3d12.h)
author: windows-sdk-content
description: Opens a handle for shared resources, shared heaps, and shared fences, by using Name and Access.
old-location: direct3d12\id3d12device_opensharedhandlebyname.htm
tech.root: direct3d12
ms.assetid: 4866BD8B-31F8-47E0-9228-5F61D6CA2190
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12Device interface,OpenSharedHandleByName method, ID3D12Device.OpenSharedHandleByName, ID3D12Device::OpenSharedHandleByName, OpenSharedHandleByName, OpenSharedHandleByName method, OpenSharedHandleByName method,ID3D12Device interface, d3d12/ID3D12Device::OpenSharedHandleByName, direct3d12.id3d12device_opensharedhandlebyname
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
 - ID3D12Device.OpenSharedHandleByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::OpenSharedHandleByName


## -description


Opens a handle for shared resources, shared heaps, and shared fences, by using Name and Access.
        


## -parameters




### -param Name [in]

Type: <b>LPCWSTR</b>

The name that was optionally passed as the <i>Name</i> parameter in the call to 
            <a href="https://msdn.microsoft.com/AFF058FF-358F-4FF3-8C92-57A9D34B27D9">ID3D12Device::CreateSharedHandle</a>.
          


### -param Access

Type: <b>DWORD</b>

The access level that was specified in the <i>Access</i> parameter in the call to 
            <a href="https://msdn.microsoft.com/AFF058FF-358F-4FF3-8C92-57A9D34B27D9">ID3D12Device::CreateSharedHandle</a>.
          


### -param pNTHandle [out]

Type: <b>HANDLE*</b>

Pointer to the shared handle.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

