---
UID: NN:d3d11_4.ID3D11Device4
title: ID3D11Device4
author: windows-sdk-content
description: The device interface represents a virtual adapter; it is used to create resources. ID3D11Device4 adds new methods to those in ID3D11Device3, such as RegisterDeviceRemovedEvent and UnregisterDeviceRemoved.
old-location: direct3d11\id3d11device4.htm
tech.root: direct3d11
ms.assetid: C4971129-C879-470A-ACD7-910D9F522E8C
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D11Device4, ID3D11Device4 interface [Direct3D 11], ID3D11Device4 interface [Direct3D 11],described, d3d11_4/ID3D11Device4, direct3d11.id3d11device4
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device4 interface


## -description


The device interface represents a virtual adapter; it is used to create resources. 
          <b>ID3D11Device4</b> adds new methods to those in <a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>, 
          such as <b>RegisterDeviceRemovedEvent</b> and <b>UnregisterDeviceRemoved</b>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device4</b> interface inherits from <a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>. <b>ID3D11Device4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Device4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6C564C67-9166-4F65-B099-3DDDECCEDC40">RegisterDeviceRemovedEvent</a>
</td>
<td align="left" width="63%">
Registers the "device removed" event and indicates when a Direct3D device has become removed for any reason, using an asynchronous notification mechanism.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F1B8BBD2-3D7D-4125-953F-D10D073B77AF">UnregisterDeviceRemoved</a>
</td>
<td align="left" width="63%">
Unregisters the "device removed" event.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>
 

 

