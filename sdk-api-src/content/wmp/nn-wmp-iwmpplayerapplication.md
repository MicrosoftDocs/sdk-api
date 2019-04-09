---
UID: NN:wmp.IWMPPlayerApplication
title: IWMPPlayerApplication (wmp.h)
author: windows-sdk-content
description: The IWMPPlayerApplication interface provides methods for switching between a remoted Windows Media Player control and the full mode of the Player. These methods can only be used with C++ programs that embed the control in remote mode.
old-location: wmp\iwmpplayerapplication.htm
tech.root: WMP
ms.assetid: bcdd7ea9-66b2-40e9-89a1-0fec073ccd92
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPPlayerApplication, IWMPPlayerApplication interface [Windows Media Player], IWMPPlayerApplication interface [Windows Media Player],described, IWMPPlayerApplicationInterface, wmp.iwmpplayerapplication, wmp/IWMPPlayerApplication
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
 - IWMPPlayerApplication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlayerApplication interface


## -description



The <b>IWMPPlayerApplication</b> interface provides methods for switching between a remoted Windows Media Player control and the full mode of the Player. These methods can only be used with C++ programs that embed the control in remote mode.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayerApplication</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPPlayerApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayerApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563528(v=VS.85).aspx">get_hasDisplay</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video can display through the remoted Windows Media Player control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563529(v=VS.85).aspx">get_playerDocked</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether Windows Media Player is in a docked state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563530(v=VS.85).aspx">switchToControl</a>
</td>
<td align="left" width="63%">
Switches a remoted Windows Media Player control to the docked state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf5a77c5-298e-48de-80cd-d7ecd9e74323">switchToPlayerApplication</a>
</td>
<td align="left" width="63%">
Switches a remoted Windows Media Player control to the full mode of the Player..

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayerApplication</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563522(v=VS.85).aspx">IWMPPlayer4</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563524(v=VS.85).aspx">get_playerApplication</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

