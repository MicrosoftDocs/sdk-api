---
UID: NN:d3d11_1.ID3D11Device1
title: ID3D11Device1
author: windows-sdk-content
description: The device interface represents a virtual adapter; it is used to create resources. ID3D11Device1 adds new methods to those in ID3D11Device.
old-location: direct3d11\id3d11device1.htm
tech.root: direct3d11
ms.assetid: DB4DAD13-3CD7-4362-950B-6403328CB071
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11Device1, ID3D11Device1 interface [Direct3D 11], ID3D11Device1 interface [Direct3D 11],described, d3d11_1/ID3D11Device1, direct3d11.id3d11device1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device1 interface


## -description


The device interface represents a virtual adapter; it is used to create resources. <b>ID3D11Device1</b> adds new methods to those in <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>. <b>ID3D11Device1</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11Device1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404577(v=VS.85).aspx">CreateBlendState1</a>
</td>
<td align="left" width="63%">
Creates a blend-state object that encapsulates blend state for the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a> and allows the configuration of logic operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404580(v=VS.85).aspx">CreateDeferredContext1</a>
</td>
<td align="left" width="63%">
Creates a deferred context, which can record command lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404583(v=VS.85).aspx">CreateDeviceContextState</a>
</td>
<td align="left" width="63%">
Creates a context state object that holds all Direct3D state and some Direct3D behavior.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404586(v=VS.85).aspx">CreateRasterizerState1</a>
</td>
<td align="left" width="63%">
Creates a rasterizer state object that informs the <a href="https://msdn.microsoft.com/en-us/library/Bb205125(v=VS.85).aspx">rasterizer stage</a> how to behave and forces the sample count while UAV rendering or rasterizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404589(v=VS.85).aspx">GetImmediateContext1</a>
</td>
<td align="left" width="63%">
Gets an immediate context, which can play back command lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404592(v=VS.85).aspx">OpenSharedResource1</a>
</td>
<td align="left" width="63%">
Gives a device access to a shared resource that is referenced by a handle and that was created on a different device. You must have previously created the resource as shared and specified that it uses NT handles (that is, you set the <a href="https://msdn.microsoft.com/en-us/library/Ff476203(v=VS.85).aspx">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404595(v=VS.85).aspx">OpenSharedResourceByName</a>
</td>
<td align="left" width="63%">
Gives a device access to a shared resource that is referenced by name and that was created on a different device. You must have previously created the resource as shared and specified that it uses NT handles (that is, you set the <a href="https://msdn.microsoft.com/en-us/library/Ff476203(v=VS.85).aspx">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag).

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>
 

 

