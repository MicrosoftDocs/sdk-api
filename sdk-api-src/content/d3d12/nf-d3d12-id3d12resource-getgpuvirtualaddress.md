---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D12Resource::GetGPUVirtualAddress


## -description



          This method returns the GPU virtual address of a buffer resource.
        


## -parameters






## -returns



Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>


            This method returns the GPU virtual address.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd synonym of UINT64.
          




## -remarks



This method is only useful for buffer resources, it will return zero for all texture resources.


          For more information on the use of GPU virtual addresses, refer to <a href="https://msdn.microsoft.com/F8D6C88A-101E-4F66-999F-43206F6527B6">Indirect Drawing</a>. 
        


#### Examples


          The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D1211on12</a> sample uses <b>ID3D12Resource::GetGPUVirtualAddress</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer-&gt;GetGPUVirtualAddress();
m_vertexBufferView.StrideInBytes = sizeof(Vertex);
m_vertexBufferView.SizeInBytes = vertexBufferSize;
</pre>
</td>
</tr>
</table></span></div>
Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>
 

 

