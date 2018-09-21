---
UID: NF:d3d12.ID3D12Device.CreateRootSignature
title: ID3D12Device::CreateRootSignature
author: windows-sdk-content
description: Creates a root signature layout.
old-location: direct3d12\id3d12device_createrootsignature.htm
tech.root: direct3d12
ms.assetid: CD3389EC-4086-40F0-B1DB-BCBCF9DDE6BA
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateRootSignature, CreateRootSignature method, CreateRootSignature method,ID3D12Device interface, ID3D12Device interface,CreateRootSignature method, ID3D12Device.CreateRootSignature, ID3D12Device::CreateRootSignature, d3d12/ID3D12Device::CreateRootSignature, direct3d12.id3d12device_createrootsignature
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
 - ID3D12Device.CreateRootSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateRootSignature


## -description


Creates a root signature layout.
        


## -parameters




### -param nodeMask [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

For single GPU operation, set this to zero. If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters) to which the root signature is to apply.
            Each bit in the mask corresponds to a single node.
            Refer to <a href="https://msdn.microsoft.com/en-us/library/Dn933253(v=VS.85).aspx">Multi-Adapter</a>.


### -param pBlobWithRootSignature [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">void</a>*</b>

A pointer to the source data for the serialized signature.
          


### -param blobLengthInBytes [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">SIZE_T</a></b>

The size, in bytes, of the block of memory that <i>pBlobWithRootSignature</i> points to.
          


### -param riid

Type: <b><b>REFIID</b></b>

The globally unique identifier (<b>GUID</b>) for the root signature interface. See Remarks.
            An input parameter.
          


### -param ppvRootSignature [out]

Type: <b><b>void</b>**</b>

A pointer to a memory block that receives a pointer to the root signature.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>.
          

This method returns <b>E_INVALIDARG</b> if the blob that <i>pBlobWithRootSignature</i> points to is invalid.
          




## -remarks



If an application procedurally generates a <a href="https://msdn.microsoft.com/en-us/library/Dn986747(v=VS.85).aspx">D3D12_ROOT_SIGNATURE_DESC</a> data structure, it must pass a pointer to this <b>D3D12_ROOT_SIGNATURE_DESC</b> in a call to <a href="https://msdn.microsoft.com/en-us/library/Dn859363(v=VS.85).aspx">D3D12SerializeRootSignature</a> to make the serialized form.
        The application then passes the serialized form to <i>pBlobWithRootSignature</i> in a call to <b>ID3D12Device::CreateRootSignature</b>.
      

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the root signature layout can be obtained by using the __uuidof() macro.
        For example, __uuidof(<a href="https://msdn.microsoft.com/BEE01381-12C2-4DD9-9121-22BB5840ECD5">ID3D12RootSignature</a>) will get the <b>GUID</b> of the interface to a root signature.
      


#### Examples

The <a href="https://msdn.microsoft.com/en-us/library/Mt186624(v=VS.85).aspx">D3D12HelloTriangle</a> sample uses <b>ID3D12Device::CreateRootSignature</b> as follows:
        

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



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn788650(v=VS.85).aspx">ID3D12Device</a>
 

 

