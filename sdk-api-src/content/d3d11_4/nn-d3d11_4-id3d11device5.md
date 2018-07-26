---
UID: NN:d3d11_4.ID3D11Device5
title: ID3D11Device5
author: windows-sdk-content
description: The device interface represents a virtual adapter; it is used to create resources. ID3D11Device5 adds new methods to those in ID3D11Device4.
old-location: direct3d11\id3d11device5.htm
old-project: direct3d11
ms.assetid: C077BAD4-08D2-4F1F-8313-5066F68F014C
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D11Device5, ID3D11Device5 interface [Direct3D 11], ID3D11Device5 interface [Direct3D 11],described, d3d11_4/ID3D11Device5, direct3d11.id3d11device5
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_4.h
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
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device5
product: Windows
targetos: Windows
req.lib: D3d11.lib
req.dll: 
req.irql: 
---

# ID3D11Device5 interface


## -description


The device interface represents a virtual adapter; it is used to create resources. <b>ID3D11Device5</b> adds new methods to those in <a href="https://msdn.microsoft.com/C4971129-C879-470A-ACD7-910D9F522E8C">ID3D11Device4</a>.
<div class="alert"><b>Note</b>  This interface, introduced in the Windows 10 Creators Update, is the latest version of the <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> interface. Applications targetting Windows 10 Creators Update should use this interface instead of earlier versions.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device5</b> interface inherits from <a href="https://msdn.microsoft.com/C4971129-C879-470A-ACD7-910D9F522E8C">ID3D11Device4</a>. <b>ID3D11Device5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Device5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B4AA9E0D-AAF4-4632-A98F-A3212764D5E1">CreateFence</a>
</td>
<td align="left" width="63%">
Creates a fence object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3EB1BA51-61CB-4389-84A9-77DAC9815AC7">OpenSharedFence</a>
</td>
<td align="left" width="63%">
Opens a handle for a shared fence by using HANDLE and REFIID.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/C4971129-C879-470A-ACD7-910D9F522E8C">ID3D11Device4</a>
 

 

