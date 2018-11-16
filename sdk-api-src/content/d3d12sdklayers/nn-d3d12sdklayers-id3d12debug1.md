---
UID: NN:d3d12sdklayers.ID3D12Debug1
title: ID3D12Debug1
author: windows-sdk-content
description: Adds GPU-Based Validation and Dependent Command Queue Synchronization to the debug layer.
old-location: direct3d12\id3d12debug1.htm
tech.root: direct3d12
ms.assetid: 3D69D0CA-5D45-49EA-BCF0-5B0ABB916261
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D12Debug1, ID3D12Debug1 interface, ID3D12Debug1 interface,described, d3d12sdklayers/ID3D12Debug1, direct3d12.id3d12debug1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d12sdklayers.h
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
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Debug1 interface


## -description


Adds GPU-Based Validation and Dependent Command Queue Synchronization to the debug layer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Debug1</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D12Debug1</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D12Debug1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt762991(v=VS.85).aspx">EnableDebugLayer</a>
</td>
<td align="left" width="63%">
Enables the debug layer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt762995(v=VS.85).aspx">SetEnableGPUBasedValidation</a>
</td>
<td align="left" width="63%">
This method enables or disables GPU-Based Validation (GBV) before creating a device with the debug layer enabled.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt762996(v=VS.85).aspx">SetEnableSynchronizedCommandQueueValidation</a>
</td>
<td align="left" width="63%">
Enables or disables dependent command queue synchronization when using a D3D12 device with the debug layer enabled.

</td>
</tr>
</table> 


## -remarks



This interface is currently in Preview mode.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950150(v=VS.85).aspx">Debug Layer Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt490477(v=VS.85).aspx">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

