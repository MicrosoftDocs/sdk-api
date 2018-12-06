---
UID: NF:d3d10sdklayers.ID3D10Debug.SetFeatureMask
title: ID3D10Debug::SetFeatureMask
author: windows-sdk-content
description: Set a bitfield of flags that will turn debug features on and off.
old-location: direct3d10\id3d10debug_setfeaturemask.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_setfeaturemask.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 663f3b21-bce6-d627-ee2d-e5e129eee88d, ID3D10Debug interface [Direct3D 10],SetFeatureMask method, ID3D10Debug.SetFeatureMask, ID3D10Debug::SetFeatureMask, SetFeatureMask, SetFeatureMask method [Direct3D 10], SetFeatureMask method [Direct3D 10],ID3D10Debug interface, d3d10sdklayers/ID3D10Debug::SetFeatureMask, direct3d10.id3d10debug_setfeaturemask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10Debug.SetFeatureMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Debug::SetFeatureMask


## -description


Set a bitfield of flags that will turn debug features on and off.


## -parameters




### -param Mask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Feature-mask flags bitwise ORed together. If a flag is present, then that feature will be set to on, otherwise the feature will be set to off. See remarks for a list of flags.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
Setting a feature-mask flag will cause a rendering-operation method (listed below) to do some extra task when called. The possible feature flags are:

<table>
<tr>
<td>D3D10_DEBUG_FEATURE_FINISH_PER_RENDER_OP</td>
<td>Application will wait for the GPU to finish processing the rendering operation before continuing.</td>
</tr>
<tr>
<td>D3D10_DEBUG_FEATURE_FLUSH_PER_RENDER_OP</td>
<td>Runtime will additionally call <a href="https://msdn.microsoft.com/3f907d7d-4316-453f-a7ea-6b228a0df569">ID3D10Device::Flush</a>.</td>
</tr>
<tr>
<td>D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP</td>
<td>Runtime will call <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>. Presentation of render buffers will occur according to the settings established by prior calls to <a href="https://msdn.microsoft.com/32efd1f4-92be-42e2-9922-15acc7df39a4">ID3D10Debug::SetSwapChain</a> and <a href="https://msdn.microsoft.com/cc724ab0-1f85-4c87-950a-3202757ba100">ID3D10Debug::SetPresentPerRenderOpDelay</a>.</td>
</tr>
</table>
 

These feature-mask flags apply to the following rendering-operation methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/01847bc8-3a58-4296-9e67-2fecd3832e48">ID3D10Device::Draw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10c4a734-6425-4bd1-ac8e-85e3255e732a">ID3D10Device::DrawIndexed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/de2cc0de-7bf3-4b03-a3de-65f841bfc228">ID3D10Device::DrawInstanced</a>
</li>
<li>
<a href="https://msdn.microsoft.com/00713e51-0bc6-4141-a10a-ab998666cdb4">ID3D10Device::DrawIndexedInstanced</a>
</li>
<li>
<a href="https://msdn.microsoft.com/22261780-2768-4ea2-9e92-57ae5560e8fe">ID3D10Device::DrawAuto</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c1a630a3-3ffe-4d6a-a8e2-7a228167adb2">ID3D10Device::ClearRenderTargetView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ac596c4d-dc54-4433-8625-defa8a04bba0">ID3D10Device::ClearDepthStencilView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/78803e46-9945-45d4-a7cc-41f527831251">ID3D10Device::CopySubresourceRegion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f3f8089-8343-4f83-9208-fd21617b8d19">ID3D10Device::CopyResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eeab4057-4827-4c4b-ae8d-1cbf1f1c9e44">ID3D10Device::UpdateSubresource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bc3491b6-99fb-4560-bce1-dd7758626cf9">ID3D10Device::GenerateMips</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cf2e9849-dbd8-4047-8e34-88fca5409bc9">ID3D10Device::ResolveSubresource</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2971189b-5df2-4d0a-ad7b-28dbfd6d0af3">ID3D10Debug Interface</a>
 

 

