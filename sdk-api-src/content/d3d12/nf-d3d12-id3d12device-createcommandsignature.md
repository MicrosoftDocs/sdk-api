---
UID: NF:d3d12.ID3D12Device.CreateCommandSignature
title: ID3D12Device::CreateCommandSignature
author: windows-sdk-content
description: This method creates a command signature.
old-location: direct3d12\id3d12device_createcommandsignature.htm
tech.root: direct3d12
ms.assetid: 5A44F907-C6E0-4548-A227-84F0CF2EE837
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateCommandSignature, CreateCommandSignature method, CreateCommandSignature method,ID3D12Device interface, ID3D12Device interface,CreateCommandSignature method, ID3D12Device.CreateCommandSignature, ID3D12Device::CreateCommandSignature, d3d12/ID3D12Device::CreateCommandSignature, direct3d12.id3d12device_createcommandsignature
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
 - ID3D12Device.CreateCommandSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateCommandSignature


## -description


This method creates a command signature.
        


## -parameters




### -param pDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/3ACB1582-7A93-4D8D-A463-A828EF0C7F92">D3D12_COMMAND_SIGNATURE_DESC</a>*</b>

Describes the command signature to be created with the <a href="https://msdn.microsoft.com/3ACB1582-7A93-4D8D-A463-A828EF0C7F92">D3D12_COMMAND_SIGNATURE_DESC</a> structure.
          


### -param pRootSignature [in, optional]

Type: <b><a href="https://msdn.microsoft.com/BEE01381-12C2-4DD9-9121-22BB5840ECD5">ID3D12RootSignature</a>*</b>

Specifies the  <a href="https://msdn.microsoft.com/BEE01381-12C2-4DD9-9121-22BB5840ECD5">ID3D12RootSignature</a> that the command signature applies to.
          

The root signature is required if any of the commands in the signature will update bindings on the pipeline. If the only command present is a draw or dispatch, the root signature parameter can be set to NULL.


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the command signature interface (<a href="https://msdn.microsoft.com/57EC15D0-9056-4AFC-86EF-3658DEA8AF40">ID3D12CommandSignature</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the command signature can be obtained by using the __uuidof() macro.
            For example, __uuidof(<b>ID3D12CommandSignature</b>) will get the <b>GUID</b> of the interface to a command signature.
          


### -param ppvCommandSignature [out, optional]

Type: <b>void**</b>

Specifies a pointer, that on successful completion of the method will point to the created command signature (<a href="https://msdn.microsoft.com/57EC15D0-9056-4AFC-86EF-3658DEA8AF40">ID3D12CommandSignature</a>).
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

