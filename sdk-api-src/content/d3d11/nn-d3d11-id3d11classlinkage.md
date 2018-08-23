---
UID: NN:d3d11.ID3D11ClassLinkage
title: ID3D11ClassLinkage
author: windows-sdk-content
description: This interface encapsulates an HLSL dynamic linkage.
old-location: direct3d11\id3d11classlinkage.htm
old-project: direct3d11
ms.assetid: eac03911-d881-4304-9598-912321ac0b0c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 6153eaad-32d7-c087-4631-725183e63035, ID3D11ClassLinkage, ID3D11ClassLinkage interface [Direct3D 11], ID3D11ClassLinkage interface [Direct3D 11],described, d3d11/ID3D11ClassLinkage, direct3d11.id3d11classlinkage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11ClassLinkage
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11ClassLinkage interface


## -description


This interface encapsulates an HLSL dynamic linkage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ClassLinkage</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>. <b>ID3D11ClassLinkage</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11ClassLinkage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476359(v=VS.85).aspx">CreateClassInstance</a>
</td>
<td align="left" width="63%">
Initializes a class-instance object that represents an HLSL class instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476360(v=VS.85).aspx">GetClassInstance</a>
</td>
<td align="left" width="63%">
Gets the class-instance object that represents the specified HLSL class.

</td>
</tr>
</table> 


## -remarks



A class linkage object can hold up to 64K gotten instances. A gotten instance is a handle that references a variable name in any shader that is created with that linkage object. When you create a shader with a class linkage object, the runtime gathers these instances and stores them in the class linkage object. For more information about how a class linkage object is used, see <a href="https://msdn.microsoft.com/en-us/library/Ff728758(v=VS.85).aspx">Storing Variables and Types for Shaders to Share</a>.

An <b>ID3D11ClassLinkage</b> object is created using the <a href="https://msdn.microsoft.com/en-us/library/Ff476502(v=VS.85).aspx">ID3D11Device::CreateClassLinkage</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476380(v=VS.85).aspx">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476161(v=VS.85).aspx">Shader Interfaces</a>
 

 

