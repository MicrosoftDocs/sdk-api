---
UID: NF:d3d12.D3D12SerializeRootSignature
title: D3D12SerializeRootSignature function
author: windows-sdk-content
description: Serializes a root signature version 1.0 that can be passed to ID3D12Device::CreateRootSignature.
old-location: direct3d12\d3d12serializerootsignature.htm
tech.root: direct3d12
ms.assetid: ACC46F5E-1074-41B3-8D13-9FD4352DBF66
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: D3D12SerializeRootSignature, D3D12SerializeRootSignature function, d3d12/D3D12SerializeRootSignature, direct3d12.d3d12serializerootsignature
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D12.dll
api_name:
 - D3D12SerializeRootSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D12SerializeRootSignature function


## -description


Serializes a root signature version 1.0 that can be passed to <a href="https://msdn.microsoft.com/en-us/library/Dn899182(v=VS.85).aspx">ID3D12Device::CreateRootSignature</a>.
        


## -parameters




### -param pRootSignature [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dn986747(v=VS.85).aspx">D3D12_ROOT_SIGNATURE_DESC</a>*</b>

The description of the root signature, as a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn986747(v=VS.85).aspx">D3D12_ROOT_SIGNATURE_DESC</a> structure.
          


### -param Version [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn899107(v=VS.85).aspx">D3D_ROOT_SIGNATURE_VERSION</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Dn899107(v=VS.85).aspx">D3D_ROOT_SIGNATURE_VERSION</a>-typed value that specifies the version of root signature.
          


### -param ppBlob [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access the serialized root signature.
          


### -param ppErrorBlob [out, optional]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that you can use to access serializer error messages, or <b>NULL</b> if there are no errors.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>.
          




## -remarks



This function has been superceded by <a href="https://msdn.microsoft.com/en-us/library/Mt709110(v=VS.85).aspx">D3D12SerializeVersionedRootSignature</a> as of the Windows 10 Anniversary Update (14393).

If an application procedurally generates a <a href="https://msdn.microsoft.com/en-us/library/Dn986747(v=VS.85).aspx">D3D12_ROOT_SIGNATURE_DESC</a> data structure, it must pass a pointer to this <b>D3D12_ROOT_SIGNATURE_DESC</b> in a call to <b>D3D12SerializeRootSignature</b> to make the serialized form.
        The application then passes the serialized form to which <i>ppBlob</i> points into <a href="https://msdn.microsoft.com/en-us/library/Dn899182(v=VS.85).aspx">ID3D12Device::CreateRootSignature</a>.
      

If a shader has been authored with a root signature in it (when that capability is added), the compiled shader will contain a serialized root signature in it already.
      

The function signature PFN_D3D12_SERIALIZE_ROOT_SIGNATURE is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      


#### Examples

Create an empty root signature.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

ComPtr&lt;ID3DBlob&gt; signature;
ComPtr&lt;ID3DBlob&gt; error;
ThrowIfFailed(D3D12SerializeRootSignature(&amp;rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &amp;signature, &amp;error));
ThrowIfFailed(m_device-&gt;CreateRootSignature(0, signature-&gt;GetBufferPointer(), signature-&gt;GetBufferSize(), IID_PPV_ARGS(&amp;m_rootSignature)));
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/en-us/library/Dn933255(v=VS.85).aspx">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770456(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn859357(v=VS.85).aspx">Creating a Root Signature</a>
 

 

