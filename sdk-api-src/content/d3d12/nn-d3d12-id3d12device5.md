---
UID: NN:d3d12.ID3D12Device5
title: ID3D12Device5
author: windows-sdk-content
description: Represents a virtual adapter. This interface extends ID3D12Device4.
old-location: direct3d12\id3d12device5.htm
tech.root: direct3d12
ms.assetid: 2D72898B-F512-4E0D-8FAC-A53EA6FE614A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D122Device5, ID3D122Device5 interface, ID3D122Device5 interface,described, ID3D12Device5, d3d12/ID3D12Device5, direct3d12.id3d12device5
ms.topic: interface
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - COM
api_location:
 - D3d12.dll
api_name:
 - ID3D122Device5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5
---

# ID3D12Device5 interface


## -description


Represents a virtual adapter. This interface extends <b>ID3D12Device4</b>.
<div class="alert"><b>Note</b>  This interface, introduced in Windows 10, version 1809, is the latest version of the <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a> interface. Applications targeting Windows 10, version 1809 and later should use this interface instead of earlier versions.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D122Device5</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12Device5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D122Device5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847458(v=VS.85).aspx">CheckDriverMatchingIdentifier</a>
</td>
<td align="left" width="63%">
Reports the compatibility of serialized data, such as a serialized raytracing acceleration structure resulting from a call to <a href="http://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure">CopyRaytracingAccelerationStructure</a> with mode  <a href="http://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_SERIALIZE</a>, with the current device/driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70AB644F-7406-4271-89C9-8D38FE3B4D7A">CreateMetaCommand</a>
</td>
<td align="left" width="63%">
Creates an instance of the specified meta command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt815644(v=VS.85).aspx">CreateStateObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/en-us/library/Mt815591(v=VS.85).aspx">ID3D12StateObject</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EA4DD3FE-E11A-4F1C-A765-4B1FCA71FB4B">EnumerateMetaCommandParameters</a>
</td>
<td align="left" width="63%">
Queries reflection metadata about the parameters of the specified meta command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71A16704-487F-49AA-B229-61CCD15B3037">EnumerateMetaCommands</a>
</td>
<td align="left" width="63%">
Queries reflection metadata about available meta commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt847459(v=VS.85).aspx">GetRaytracingAccelerationStructurePrebuildInfo</a>
</td>
<td align="left" width="63%">
Query the driver for resource requirements to build an acceleration structure. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>



<a href="https://msdn.microsoft.com/7650C695-3F46-405A-9976-A4A50FFAD567">ID3D12Device1</a>



<a href="https://msdn.microsoft.com/86C46FD2-7B1D-4F66-97F7-45F9428C5E1E">ID3D12Device2</a>



<a href="https://msdn.microsoft.com/038E546C-4000-401A-8A11-7A83F391676E">ID3D12Device3</a>
 

 

