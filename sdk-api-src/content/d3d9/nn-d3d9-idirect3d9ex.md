---
UID: NN:d3d9.IDirect3D9Ex
title: IDirect3D9Ex
author: windows-sdk-content
description: Applications use the methods of the IDirect3D9Ex interface (which inherits from IDirect3D9) to create Microsoft Direct3D 9Ex objects and set up the environment.
old-location: direct3d9\idirect3d9ex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 88878a9a-f85c-f0f1-6268-c5b3e11bb875, IDirect3D9Ex, IDirect3D9Ex interface [Direct3D 9], IDirect3D9Ex interface [Direct3D 9],described, d3d9/IDirect3D9Ex, direct3d9.idirect3d9ex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3D9Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3D9Ex interface


## -description


Applications use the methods of the <b>IDirect3D9Ex</b> interface (which inherits from <a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>) to create Microsoft Direct3D 9Ex objects and set up the environment. This interface includes methods for enumerating and retrieving capabilities of the device and is available when the underlying device implementation is compliant with Windows Vista.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3D9Ex</b> interface inherits from <a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>. <b>IDirect3D9Ex</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3D9Ex</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7182c5ea-40ca-4cf8-a33e-b22984fc9349">CreateDeviceEx</a>
</td>
<td align="left" width="63%">
Creates a device to represent the display adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39ead901-80ad-498c-951a-b39e498ac052">EnumAdapterModesEx</a>
</td>
<td align="left" width="63%">
This method returns the actual display mode info based on the given mode index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c083fc7-85cf-4ea0-bb14-ee652231eb42">GetAdapterDisplayModeEx</a>
</td>
<td align="left" width="63%">
Retrieves the current display mode and rotation settings of the adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3960ab37-3471-4f9b-be99-0c33a9f89c9f">GetAdapterLUID</a>
</td>
<td align="left" width="63%">
This method returns a unique identifier for the adapter that is specific to the adapter hardware. Applications can use this identifier to define robust mappings across various APIs (Direct3D 9, DXGI).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdd2f2a3-44b6-4b82-bae3-11450ff2a415">GetAdapterModeCountEx</a>
</td>
<td align="left" width="63%">
Returns the number of display modes available.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3D9Ex</b> interface is obtained by calling the <a href="https://msdn.microsoft.com/5480ecab-9820-4352-9587-4eba6ab26ebf">Direct3DCreate9Ex</a> function.

The <b>LPDIRECT3D9EX</b> and <b>PDIRECT3D9EX</b> types are defined as pointers to the <b>IDirect3D9Ex</b> interface:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3D9Ex *LPDIRECT3D9EX, *PDIRECT3D9EX;
</pre>
</td>
</tr>
</table></span></div>





## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

