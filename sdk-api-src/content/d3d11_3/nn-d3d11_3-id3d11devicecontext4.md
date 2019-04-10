---
UID: NN:d3d11_3.ID3D11DeviceContext4
title: ID3D11DeviceContext4 (d3d11_3.h)
author: windows-sdk-content
description: The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext4 adds new methods to those in ID3D11DeviceContext3.
old-location: direct3d11\id3d11devicecontext4.htm
tech.root: direct3d11
ms.assetid: 9A4B737C-C0A8-4319-A9CA-8172E992774D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext4, ID3D11DeviceContext4 interface [Direct3D 11], ID3D11DeviceContext4 interface [Direct3D 11],described, d3d11_3/ID3D11DeviceContext4, direct3d11.id3d11devicecontext4
ms.topic: interface
req.header: d3d11_3.h
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
 - ID3D11DeviceContext4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext4 interface


## -description


The device context interface represents a device context; it is used to render commands. <b>ID3D11DeviceContext4</b> adds new methods to those in <a href="https://msdn.microsoft.com/65F462DB-5546-4B23-B438-60067FD60103">ID3D11DeviceContext3</a>.
<div class="alert"><b>Note</b>  This interface, introduced in the Windows 10 Creators Update, is the latest version of the <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a> interface. Applications targetting Windows 10 Creators Update should use this interface instead of earlier versions.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext4</b> interface inherits from <a href="https://msdn.microsoft.com/65F462DB-5546-4B23-B438-60067FD60103">ID3D11DeviceContext3</a>. <b>ID3D11DeviceContext4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11DeviceContext4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5B308187-27B1-40B8-B9B7-CD8A8223A0EE">Signal</a>
</td>
<td align="left" width="63%">
Updates a fence to a specified value after all previous work has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91576E2D-A28F-43A8-B9FE-5888779877F9">Wait</a>
</td>
<td align="left" width="63%">
Waits until the specified fence reaches or exceeds the specified value before future work can begin.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContect2</a>



<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>



<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>



<a href="https://msdn.microsoft.com/65F462DB-5546-4B23-B438-60067FD60103">ID3D11DeviceContext3</a>
 

 

