---
UID: NN:wmp.IWMPPlayerServices2
title: IWMPPlayerServices2
author: windows-sdk-content
description: The IWMPPlayerServices2 interface provides a method used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player.
old-location: wmp\iwmpplayerservices2.htm
tech.root: WMP
ms.assetid: abbce425-9185-4235-8d8e-28be591be8e5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlayerServices2, IWMPPlayerServices2 interface [Windows Media Player], IWMPPlayerServices2 interface [Windows Media Player],described, IWMPPlayerServices2Interface, wmp.iwmpplayerservices2, wmp/IWMPPlayerServices2
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMPPlayerServices2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlayerServices2 interface


## -description



The <b>IWMPPlayerServices2</b> interface provides a method used by the host of a remoted Windows Media Player control to manipulate the full mode of the Player. In addition to the methods inherited from <b>IWMPPlayerServices</b>, the <b>IWMPPlayerServices2</b> interface exposes the following methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayerServices2</b> interface inherits from <a href="https://msdn.microsoft.com/abbce425-9185-4235-8d8e-28be591be8e5">IWMPPlayerServices2</a>. <b>IWMPPlayerServices2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayerServices2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e3536d2-006b-4019-a9c5-c460135cf555">setBackgroundProcessingPriority</a>
</td>
<td align="left" width="63%">
Specifies a priority level for general background processing tasks.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayerServices2</b> interface by calling the COM <b>CoCreateInstance</b> method.
	


## -see-also




<a href="https://msdn.microsoft.com/3d9ca91f-c672-4ecb-a6db-67d7e1ddbe7e">IWMPPlayerServices Interface</a>



<a href="https://msdn.microsoft.com/abbce425-9185-4235-8d8e-28be591be8e5">IWMPPlayerServices2</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

