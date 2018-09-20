---
UID: NN:d3d11.ID3D11ClassInstance
title: ID3D11ClassInstance
author: windows-sdk-content
description: This interface encapsulates an HLSL class.
old-location: direct3d11\id3d11classinstance.htm
tech.root: direct3d11
ms.assetid: 70d006d2-5c47-4e8a-9a14-b5475d88ac32
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D11ClassInstance, ID3D11ClassInstance interface [Direct3D 11], ID3D11ClassInstance interface [Direct3D 11],described, d3d11/ID3D11ClassInstance, direct3d11.id3d11classinstance, fb695194-ccb6-d8bd-59c0-5dbd185a1a4c
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11ClassInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ClassInstance interface


## -description


This interface encapsulates an HLSL class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ClassInstance</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11ClassInstance</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11ClassInstance</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06e5b132-5f20-41e1-827a-26df989cd4f0">GetClassLinkage</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a> object associated with the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5062595c-4152-4cfd-afcd-3e51d1087675">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a description of the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e9c3410-6421-4300-b3a6-de4840a81117">GetInstanceName</a>
</td>
<td align="left" width="63%">
Gets the instance name of the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a46699b5-2250-442a-85ab-37eeb419ac72">GetTypeName</a>
</td>
<td align="left" width="63%">
Gets the type of the current HLSL class.

</td>
</tr>
</table> 


## -remarks



This interface is created by calling <a href="https://msdn.microsoft.com/26e5b1c7-d7b7-413b-a072-33f8f5dd5d3f">ID3D11ClassLinkage::CreateClassInstance</a>. The interface is used when binding shader resources to the pipeline using APIs such as <a href="https://msdn.microsoft.com/d6207779-7477-4e74-beb8-065949abce06">ID3D11DeviceContext::VSSetShader</a>.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

