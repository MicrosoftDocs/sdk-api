---
UID: NN:d3d11_3.ID3D11DeviceContext3
title: ID3D11DeviceContext3
author: windows-sdk-content
description: The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext3 adds new methods to those in ID3D11DeviceContext2.
old-location: direct3d11\id3d11devicecontext3.htm
tech.root: direct3d11
ms.assetid: 65F462DB-5546-4B23-B438-60067FD60103
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D11DeviceContext3, ID3D11DeviceContext3 interface [Direct3D 11], ID3D11DeviceContext3 interface [Direct3D 11],described, d3d11_3/ID3D11DeviceContext3, direct3d11.id3d11devicecontext3
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D11DeviceContext3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext3 interface


## -description


The device context interface represents a device context; it is used to render commands. 
        <b>ID3D11DeviceContext3</b> adds new methods to those in <a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext3</b> interface inherits from <a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>. <b>ID3D11DeviceContext3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11DeviceContext3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DBDA19C3-EC4E-4C12-B1ED-A92E5CE28CED">Flush1</a>
</td>
<td align="left" width="63%">
Sends queued-up commands in the command buffer to the graphics processing unit (GPU), with a specified context type and an optional event handle to create an event query.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52D1F2B2-DBC9-4714-A9C5-A0283EA6C5B7">GetHardwareProtectionState</a>
</td>
<td align="left" width="63%">
Gets whether hardware protection is enabled.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C1B927EC-32A2-4526-9F30-739D21C7E4A6">SetHardwareProtectionState</a>
</td>
<td align="left" width="63%">
Sets the hardware protection state.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>



<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>



<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>
 

 

