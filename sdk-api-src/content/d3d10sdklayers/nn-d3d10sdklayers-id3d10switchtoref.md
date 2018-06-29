---
UID: NN:d3d10sdklayers.ID3D10SwitchToRef
title: ID3D10SwitchToRef
author: windows-sdk-content
description: A switch-to-reference interface (see the switch-to-reference layer) enables an application to switch between a hardware and software device.
old-location: direct3d10\id3d10switchtoref.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10switchtoref.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ID3D10SwitchToRef, ID3D10SwitchToRef interface [Direct3D 10], ID3D10SwitchToRef interface [Direct3D 10],described, d3d10sdklayers/ID3D10SwitchToRef, d7769c3f-e1b2-ded4-9352-be26f55a05d1, direct3d10.id3d10switchtoref
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10SwitchToRef
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10SwitchToRef interface


## -description


A switch-to-reference interface (see the <a href="https://msdn.microsoft.com/library/Bb205068(v=VS.85).aspx">switch-to-reference</a> layer) enables an application to switch between a hardware and software device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10SwitchToRef</b> interface inherits from <a href="https://msdn.microsoft.com/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>. <b>ID3D10SwitchToRef</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10SwitchToRef</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173861(v=VS.85).aspx">GetUseRef</a>
</td>
<td align="left" width="63%">
Get a boolean value that indicates the type of device being used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb173862(v=VS.85).aspx">SetUseRef</a>
</td>
<td align="left" width="63%">
Switch between a hardware and a software device.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on a <a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a> created with the <a href="https://msdn.microsoft.com/library/Bb204909(v=VS.85).aspx">D3D10_CREATE_DEVICE_SWITCH_TO_REF</a> flag.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205152(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>
 

 

