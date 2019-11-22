---
UID: NN:d3d10effect.ID3D10StateBlock
title: ID3D10StateBlock (d3d10effect.h)

description: A state-block interface encapsulates render states.
old-location: direct3d10\id3d10stateblock.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10stateblock.htm

ms.date: 12/05/2018
ms.keywords: 23872e09-b63b-11d0-bb95-f57009f0fab6, ID3D10StateBlock, ID3D10StateBlock interface [Direct3D 10], ID3D10StateBlock interface [Direct3D 10],described, d3d10effect/ID3D10StateBlock, direct3d10.id3d10stateblock
ms.topic: interface
f1_keywords: 
 - "d3d10effect/ID3D10StateBlock"
dev_langs:
 - c++
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10StateBlock interface


## -description


A state-block interface encapsulates render states.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10StateBlock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10StateBlock</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10stateblock-apply">Apply</a>
</td>
<td align="left" width="63%">
Apply the state block to the current device state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10stateblock-capture">Capture</a>
</td>
<td align="left" width="63%">
Capture the current value of states that are included in a stateblock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10stateblock-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Get the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10stateblock-releasealldeviceobjects">ReleaseAllDeviceObjects</a>
</td>
<td align="left" width="63%">
Release all references to device objects.

</td>
</tr>
</table> 


## -remarks



To create a state-block interface, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-d3d10createstateblock">D3D10CreateStateBlock</a>.

This interface can be used to save and restore pipeline state. It can also be used to capture the current state.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>
 

 

