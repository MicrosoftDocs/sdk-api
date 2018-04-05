---
UID: NN:d3d11_1.ID3D11DeviceContext1
title: ID3D11DeviceContext1
author: windows-driver-content
description: The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext1 adds new methods to those in ID3D11DeviceContext.
old-location: direct3d11\id3d11devicecontext1.htm
old-project: direct3d11
ms.assetid: DD2A556D-AEF0-407E-A497-CF17ACDEB1A7
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D11DeviceContext1, ID3D11DeviceContext1 interface [Direct3D 11], ID3D11DeviceContext1 interface [Direct3D 11], described, d3d11_1/ID3D11DeviceContext1, direct3d11.id3d11devicecontext1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext1 interface


## -description


The device context interface represents a device context; it is used to render commands. <b>ID3D11DeviceContext1</b> adds new methods to those in <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext1</b> interface inherits from <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>. <b>ID3D11DeviceContext1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11DeviceContext1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7CC8DEB6-075C-40EB-822D-8A627E285FA2">ClearView</a>
</td>
<td align="left" width="63%">
Sets all the elements in a resource view to one value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1963011F-C3E2-428D-B667-195A4976510B">CopySubresourceRegion1</a>
</td>
<td align="left" width="63%">
Copies a region from a source resource to a destination resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B729FEF6-44AA-4F1B-A73B-000C3691F232">CSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the compute-shader stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52524F23-8196-47DB-A57C-F7214BC23BE8">CSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the compute-shader stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6C27231E-BF61-4D50-B5B1-59961B82534B">DiscardResource</a>
</td>
<td align="left" width="63%">
Discards a resource from the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7BBF20BC-3777-46B9-8DE3-40B7B88DAF6C">DiscardView</a>
</td>
<td align="left" width="63%">
Discards a resource view from the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C478F696-D0D7-4ABB-8BCD-5C528CC13814">DiscardView1</a>
</td>
<td align="left" width="63%">
Discards the specified elements in a resource view from the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7C6E2BFF-E351-417C-B351-F9B8EDB95F57">DSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the domain-shader stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3B37B2AE-96E8-4275-B9D9-7CA8D027C6E1">DSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the domain-shader stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5899782E-89A4-4DFD-8A1E-AA7E87364AFC">GSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the geometry shader pipeline stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6C15F822-9F02-4CC9-8B69-60D902ACEB88">GSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the geometry shader pipeline stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/600F04B5-2173-4CB0-9978-7A0327BE1FE0">HSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull-shader stage</a> uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8E44A677-8C08-4343-BFA4-D4B536DB082B">HSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull-shader stage</a> of the pipeline uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68BCB27D-5D31-45BC-87BD-47E083F75933">PSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the pixel shader pipeline stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4B05144B-7766-4AE6-9B9F-C439B4BF0220">PSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">

        Sets the constant buffers that the pixel shader pipeline stage uses, and enables the shader to access other parts of the buffer.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4E267E86-602F-459C-A6F9-4660EC8FA752">SwapDeviceContextState</a>
</td>
<td align="left" width="63%">
Activates the given context state object and changes the current device behavior to Direct3D 11, Direct3D 10.1, or Direct3D 10.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7D89591C-F3F7-4A4F-A91A-AC67D9A573AF">UpdateSubresource1</a>
</td>
<td align="left" width="63%">
The CPU copies data from memory to a subresource created in non-mappable memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5499AA20-0B1C-4F01-9059-0092D689DE73">VSGetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Gets the constant buffers that the vertex shader pipeline stage uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4D896539-216F-4823-B36E-2FE3E8A40C64">VSSetConstantBuffers1</a>
</td>
<td align="left" width="63%">
Sets the constant buffers that the vertex shader pipeline stage uses.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

