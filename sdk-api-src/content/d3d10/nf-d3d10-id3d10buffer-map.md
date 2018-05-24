---
UID: NF:d3d10.ID3D10Buffer.Map
title: ID3D10Buffer::Map
author: windows-driver-content
description: Get a pointer to the data contained in the resource and deny GPU access to the resource.
old-location: direct3d10\id3d10buffer_map.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10buffer_map.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 7d41a2a2-1ba6-cc42-c30b-821d5734b5c3, ID3D10Buffer interface [Direct3D 10],Map method, ID3D10Buffer.Map, ID3D10Buffer::Map, Map, Map method [Direct3D 10], Map method [Direct3D 10],ID3D10Buffer interface, d3d10/ID3D10Buffer::Map, direct3d10.id3d10buffer_map
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Buffer.Map
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Buffer::Map


## -description


Get a pointer to the data contained in the resource and deny GPU access to the resource.


## -parameters




### -param MapType [in]

Type: <b><a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP</a></b>

Flag that specifies the CPU's permissions for the reading and writing of a resource. For possible values, see <a href="https://msdn.microsoft.com/6a8e10cf-2cab-41f0-ba43-afa6854477ff">D3D10_MAP</a>.


### -param MapFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flag that specifies what the CPU should do when the GPU is busy (see <a href="https://msdn.microsoft.com/cc8a1dae-4a48-4894-8ef4-67289062400d">D3D10_MAP_FLAG</a>). This flag is optional.


### -param ppData [out]

Type: <b>void**</b>

Pointer to the buffer resource data.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this function succeeds, it returns S_OK. The following list contains some of the reasons that <b>Map</b> can fail:
      

<ul>
<li>If <i>MapFlags</i> specifies D3D10_MAP_FLAG_DO_NOT_WAIT and the GPU is not yet finished with the resource, <b>ID3D10Buffer::Map</b> 
        returns DXGI_ERROR_WAS_STILL_DRAWING.</li>
<li><b>ID3D10Buffer::Map</b> returns DXGI_ERROR_DEVICE_REMOVED if <i>MapType</i> includes any flags that permit reading and the hardware 
        device (that is, the video card) has been removed.</li>
</ul>
For more information about the preceding return values, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



For the CPU to write the contents of a resource, the resource must be created with the dynamic usage flag, D3D10_USAGE_DYNAMIC. 
      To both read and write those contents, the resource must be created with the staging usage flag, D3D10_USAGE_STAGING. (For more information about 
      these flags, see <a href="https://msdn.microsoft.com/eaaf695c-e99d-4bf8-b479-fa2d06d53248">D3D10_USAGE</a>.) <b>ID3D10Buffer::Map</b> will retrieve a pointer to the resource data. 
      For a discussion on how to access resources efficiently, see <a href="https://msdn.microsoft.com/34fd4d15-ee64-4acf-967d-a4afb6f26329">Copying and Accessing Resource Data (Direct3D 10)</a>.

Call <a href="https://msdn.microsoft.com/b6636c07-0e09-4c95-bab3-357ed4ebe0b8">ID3D10Buffer::Unmap</a> to signify that the application has finished accessing the resource.

<b>ID3D10Buffer::Map</b> has a few other restrictions. For example:

<ul>
<li>The same buffer cannot be mapped multiple times; in other words, do not call <b>ID3D10Buffer::Map</b> on a buffer that is already mapped.</li>
<li>Any buffer that is bound to the pipeline must be unmapped before any rendering operation (that is, <a href="https://msdn.microsoft.com/01847bc8-3a58-4296-9e67-2fecd3832e48">ID3D10Device::Draw</a>) 
        can be executed.</li>
</ul>
<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

<b>ID3D10Buffer::Map</b> in Direct3D 10 is analogous to resource <a href="https://msdn.microsoft.com/b17d8262-e514-4b9c-9237-653a4258a14e">Lock</a> in Direct3D 9.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer Interface</a>
 

 

