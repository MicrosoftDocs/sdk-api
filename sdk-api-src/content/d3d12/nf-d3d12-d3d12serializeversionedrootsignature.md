---
UID: NF:d3d12.D3D12SerializeVersionedRootSignature
title: D3D12SerializeVersionedRootSignature function (d3d12.h)
author: windows-sdk-content
description: Serializes a root signature of any version that can be passed to ID3D12Device::CreateRootSignature.
old-location: direct3d12\d3d12serializeversionedrootsignature.htm
tech.root: direct3d12
ms.assetid: D8A15561-4911-4067-B25E-8BF2B079FD81
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12SerializeVersionedRootSignature, D3D12SerializeVersionedRootSignature function, d3d12/D3D12SerializeVersionedRootSignature, direct3d12.d3d12serializeversionedrootsignature
ms.topic: function
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3d12.dll
api_name:
 - D3D12SerializeVersionedRootSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D12SerializeVersionedRootSignature function


## -description


Serializes a root signature of any version that can be passed to <a href="https://msdn.microsoft.com/CD3389EC-4086-40F0-B1DB-BCBCF9DDE6BA">ID3D12Device::CreateRootSignature</a>.
        


## -parameters




### -param pRootSignature [in]

Type: <b>const <a href="https://msdn.microsoft.com/46F692DD-55FF-4DFF-AF11-78CAD10922C1">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a>*</b>

Specifies a <a href="https://msdn.microsoft.com/46F692DD-55FF-4DFF-AF11-78CAD10922C1">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a> that contains a description of any version of a root signature.


### -param ppBlob [out]

Type: <b>ID3DBlob**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access the serialized root signature.
          


### -param ppErrorBlob [out, optional]

Type: <b>ID3DBlob**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access serializer error messages, or <b>NULL</b> if there are no errors.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



If an application procedurally generates a <a href="https://msdn.microsoft.com/F085D077-1DA8-41A1-9FA3-4423EA003345">D3D12_ROOT_SIGNATURE_DESC1</a> data structure, it must pass a pointer to this <b>D3D12_ROOT_SIGNATURE_DESC1</b> in a call to <b>D3D12SerializeVersionedRootSignature</b> to make the serialized form.
        The application then passes the serialized form to which <i>ppBlob</i> points into <a href="https://msdn.microsoft.com/CD3389EC-4086-40F0-B1DB-BCBCF9DDE6BA">ID3D12Device::CreateRootSignature</a>.
      

If a shader has been authored with a root signature in it (when that capability is added), the compiled shader will contain a serialized root signature in it already.
      

The function signature PFN_D3D12_SERIALIZE_VERSIONED_ROOT_SIGNATURE is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      

This function was released with the Windows 10 Anniversary Update (14393) and supersedes <a href="https://msdn.microsoft.com/ACC46F5E-1074-41B3-8D13-9FD4352DBF66">D3D12SerializeRootSignature</a>.




## -see-also




<a href="https://msdn.microsoft.com/C0F9A52C-483D-40B2-9E1F-CB92ADDC2856">Core Functions</a>



<a href="https://msdn.microsoft.com/565B28C1-DBD1-42B6-87F9-70743E4A2E4A">Creating a Root Signature</a>



<a href="https://msdn.microsoft.com/0F6BA6C1-9A33-4E99-BF34-4A0358E7427D">D3DX12SerializeVersionedRootSignature</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>
 

 

