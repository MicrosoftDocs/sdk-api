---
UID: NN:wmp.IWMPRemoteMediaServices
title: IWMPRemoteMediaServices
author: windows-sdk-content
description: The IWMPRemoteMediaServices interface includes methods that provide services to Windows Media Player from a program that hosts the Player control. These methods are designed to be used with C++, and some methods can only be used with remoting.
old-location: wmp\iwmpremotemediaservices.htm
tech.root: WMP
ms.assetid: 594a614a-8da1-4ef0-a6af-01284fb48ef7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPRemoteMediaServices, IWMPRemoteMediaServices interface [Windows Media Player], IWMPRemoteMediaServices interface [Windows Media Player],described, IWMPRemoteMediaServicesInterface, wmp.iwmpremotemediaservices, wmp/IWMPRemoteMediaServices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmp.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPRemoteMediaServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPRemoteMediaServices interface


## -description



The <b>IWMPRemoteMediaServices</b> interface includes methods that provide services to Windows Media Player from a program that hosts the Player control. These methods are designed to be used with C++, and some methods can only be used with remoting.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPRemoteMediaServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPRemoteMediaServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPRemoteMediaServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3a210f9-90ea-4a6e-8aab-9e8cd7e21ab6">GetApplicationName</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve the name of the program that is hosting the remoted control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/892c2513-9ca2-48fe-b745-0fdc0f445871">GetCustomUIMode</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve the location of a skin file to apply to the Player control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2e313fd-cbf6-4b0f-8eb0-1097af53e77a">GetScriptableObject</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve a name and interface pointer for an object that can be called from the script code within a skin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/866e7ee7-5df1-4e6b-8b41-85c6ff8b64d5">GetServiceType</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to determine whether a host program wants to run its embedded control remotely.

</td>
</tr>
</table> 

A pointer to an <b>IWMPRemoteMediaServices</b> interface is retrieved by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

