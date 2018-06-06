---
UID: NN:d3d11.ID3D11Asynchronous
title: ID3D11Asynchronous
author: windows-sdk-content
description: This interface encapsulates methods for retrieving data from the GPU asynchronously.
old-location: direct3d11\id3d11asynchronous.htm
old-project: direct3d11
ms.assetid: 37ff9dc0-5ec2-4cd5-b252-44e2dac45355
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11Asynchronous, ID3D11Asynchronous interface [Direct3D 11], ID3D11Asynchronous interface [Direct3D 11],described, ba273b1e-153b-fd26-ff4e-e9755f4ea1f2, d3d11/ID3D11Asynchronous, direct3d11.id3d11asynchronous
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
 - ID3D11Asynchronous
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Asynchronous interface


## -description


This interface encapsulates methods for retrieving data from the GPU asynchronously.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Asynchronous</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11Asynchronous</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Asynchronous</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8766ca9f-b15e-4608-9fcd-c1b4fcda5e8d">GetDataSize</a>
</td>
<td align="left" width="63%">
Get the size of the data (in bytes) that is output when calling <a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">ID3D11DeviceContext::GetData</a>.

</td>
</tr>
</table> 


## -remarks



There are three types of asynchronous interfaces, all of which inherit this interface:

<ul>
<li>
<a href="https://msdn.microsoft.com/d296a5aa-147c-460d-acc6-e097ea503378">ID3D11Query</a> - Queries information from the GPU.</li>
<li>
<a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a> - Determines whether a piece of geometry should be processed or not depending on the results of a previous draw call.</li>
<li>
<a href="https://msdn.microsoft.com/3f35b3d5-f829-443c-9ea6-6cffdd4f58b7">ID3D11Counter</a> - Measures GPU performance.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

