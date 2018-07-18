---
UID: NN:d3d10effect.ID3D10StateBlock
title: ID3D10StateBlock
author: windows-sdk-content
description: A state-block interface encapsulates render states.
old-location: direct3d10\id3d10stateblock.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10stateblock.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 23872e09-b63b-11d0-bb95-f57009f0fab6, ID3D10StateBlock, ID3D10StateBlock interface [Direct3D 10], ID3D10StateBlock interface [Direct3D 10],described, d3d10effect/ID3D10StateBlock, direct3d10.id3d10stateblock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10effect.h
req.include-header: D3D10.h
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10StateBlock
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10StateBlock interface


## -description


A state-block interface encapsulates render states.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10StateBlock</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10StateBlock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10StateBlock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b5351ef-b2cd-4c80-a1ee-6e2b25d007b8">Apply</a>
</td>
<td align="left" width="63%">
Apply the state block to the current device state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea55f168-dbb0-40de-908f-e8a4418894ae">Capture</a>
</td>
<td align="left" width="63%">
Capture the current value of states that are included in a stateblock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451305">GetDevice</a>
</td>
<td align="left" width="63%">
Get the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4f64351-214e-4ce0-ad3b-04053a7cb8e6">ReleaseAllDeviceObjects</a>
</td>
<td align="left" width="63%">
Release all references to device objects.

</td>
</tr>
</table> 


## -remarks



To create a state-block interface, call <a href="https://msdn.microsoft.com/a6d3ed76-5321-4876-a95f-dc5c7302e76f">D3D10CreateStateBlock</a>.

This interface can be used to save and restore pipeline state. It can also be used to capture the current state.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>
 

 

