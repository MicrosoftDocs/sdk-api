---
UID: NF:d3d11on12.ID3D11On12Device.CreateWrappedResource
title: ID3D11On12Device::CreateWrappedResource
author: windows-sdk-content
description: This method creates D3D11 resources for use with D3D 11on12.
old-location: direct3d12\id3d11on12device_createwrappedresource.htm
old-project: direct3d12
ms.assetid: 83B37B0A-9965-40F6-A5B1-8B4DC21BC455
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CreateWrappedResource, CreateWrappedResource method, CreateWrappedResource method,ID3D11On12Device interface, ID3D11On12Device interface,CreateWrappedResource method, ID3D11On12Device.CreateWrappedResource, ID3D11On12Device::CreateWrappedResource, d3d11on12/ID3D11On12Device::CreateWrappedResource, direct3d12.id3d11on12device_createwrappedresource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11on12.h
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
tech.root: 
req.typenames: D3D11_AES_CTR_IV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11On12Device.CreateWrappedResource
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
---

# ID3D11On12Device::CreateWrappedResource


## -description



          This method creates D3D11 resources for use with D3D 11on12.
        


## -parameters




### -param pResource12 [in]

Type: <b>IUnknown*</b>


            A pointer to an already-created D3D12 resource or heap.
          


### -param pFlags11 [in]

Type: <b>const <a href="https://msdn.microsoft.com/50C1ACA1-714C-467A-A548-B5EE50DA3E3D">D3D11_RESOURCE_FLAGS</a>*</b>


              A <a href="https://msdn.microsoft.com/50C1ACA1-714C-467A-A548-B5EE50DA3E3D">D3D11_RESOURCE_FLAGS</a> structure that enables an application to override flags that would be inferred by the resource/heap properties.
              The D3D11_RESOURCE_FLAGS structure contains bind flags, misc flags, and CPU access flags.
            


### -param InState

Type: <b><a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a></b>


            The use of the resource on input, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
          


### -param OutState

Type: <b><a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a></b>


            The use of the resource on output, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> enumeration constants.
          


### -param riid

Type: <b>REFIID</b>


            The globally unique identifier (<b>GUID</b>) for the wrapped resource interface.
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the wrapped resource can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>) will get the <b>GUID</b> of the interface to a wrapped resource.
          


### -param ppResource11 [out, optional]

Type: <b>void**</b>


            After the method returns, points to the newly created wrapped D3D11 resource or heap.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/031F9AC2-E5C0-47F9-B084-2D2431F1187A">ID3D11On12Device</a>
 

 

