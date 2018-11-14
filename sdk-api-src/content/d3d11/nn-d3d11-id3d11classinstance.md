---
UID: NN:d3d11.ID3D11ClassInstance
title: ID3D11ClassInstance
author: windows-sdk-content
description: This interface encapsulates an HLSL class.
old-location: direct3d11\id3d11classinstance.htm
tech.root: direct3d11
ms.assetid: 70d006d2-5c47-4e8a-9a14-b5475d88ac32
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11ClassInstance, ID3D11ClassInstance interface [Direct3D 11], ID3D11ClassInstance interface [Direct3D 11],described, d3d11/ID3D11ClassInstance, direct3d11.id3d11classinstance, fb695194-ccb6-d8bd-59c0-5dbd185a1a4c
ms.prod: windows-hardware
ms.technology: windows-devices
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ClassInstance</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11ClassInstance</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ff476354(v=VS.85).aspx">GetClassLinkage</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/en-us/library/Ff476358(v=VS.85).aspx">ID3D11ClassLinkage</a> object associated with the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476355(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Gets a description of the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476356(v=VS.85).aspx">GetInstanceName</a>
</td>
<td align="left" width="63%">
Gets the instance name of the current HLSL class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476357(v=VS.85).aspx">GetTypeName</a>
</td>
<td align="left" width="63%">
Gets the type of the current HLSL class.

</td>
</tr>
</table> 


## -remarks



This interface is created by calling <a href="https://msdn.microsoft.com/en-us/library/Ff476359(v=VS.85).aspx">ID3D11ClassLinkage::CreateClassInstance</a>. The interface is used when binding shader resources to the pipeline using APIs such as <a href="https://msdn.microsoft.com/en-us/library/Ff476493(v=VS.85).aspx">ID3D11DeviceContext::VSSetShader</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476161(v=VS.85).aspx">Shader Interfaces</a>
 

 

