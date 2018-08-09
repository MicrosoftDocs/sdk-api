---
UID: NN:wmp.IWMPPlayerApplication
title: IWMPPlayerApplication
author: windows-sdk-content
description: The IWMPPlayerApplication interface provides methods for switching between a remoted Windows Media Player control and the full mode of the Player. These methods can only be used with C++ programs that embed the control in remote mode.
old-location: wmp\iwmpplayerapplication.htm
old-project: WMP
ms.assetid: bcdd7ea9-66b2-40e9-89a1-0fec073ccd92
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlayerApplication, IWMPPlayerApplication interface [Windows Media Player], IWMPPlayerApplication interface [Windows Media Player],described, IWMPPlayerApplicationInterface, wmp.iwmpplayerapplication, wmp/IWMPPlayerApplication
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
tech.root: 
req.typenames: WMPSyncState
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayerApplication interface


## -description



The <b>IWMPPlayerApplication</b> interface provides methods for switching between a remoted Windows Media Player control and the full mode of the Player. These methods can only be used with C++ programs that embed the control in remote mode.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayerApplication</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPPlayerApplication</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a356929a-51de-49b6-bf7a-b3bd7fa35ea2">get_hasDisplay</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video can display through the remoted Windows Media Player control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca590b80-433d-4a9f-9d6b-cbb33d328fda">get_playerDocked</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether Windows Media Player is in a docked state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15be3a28-4e51-46bf-bb64-e45e20ae3524">switchToControl</a>
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
<a href="https://msdn.microsoft.com/afe5dbd1-96e1-4abe-b843-ec6130fa02d0">IWMPPlayer4</a>
</td>
<td>
<a href="https://msdn.microsoft.com/37b4b0b1-f16e-42ed-830e-9b0468a66eeb">get_playerApplication</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

