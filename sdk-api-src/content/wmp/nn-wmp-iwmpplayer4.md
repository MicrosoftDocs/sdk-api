---
UID: NN:wmp.IWMPPlayer4
title: IWMPPlayer4
author: windows-sdk-content
description: The IWMPPlayer4 interface provides methods for modifying the basic behavior of the Windows Media Player control user interface.
old-location: wmp\iwmpplayer4.htm
tech.root: WMP
ms.assetid: afe5dbd1-96e1-4abe-b843-ec6130fa02d0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPlayer4, IWMPPlayer4 interface [Windows Media Player], IWMPPlayer4 interface [Windows Media Player],described, IWMPPlayer4Interface, wmp.iwmpplayer4, wmp/IWMPPlayer4
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
 - IWMPPlayer4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlayer4 interface


## -description



The <b>IWMPPlayer4</b> interface provides methods for modifying the basic behavior of the Windows Media Player control user interface. These methods supplement the <b>IWMPCore3</b> interface.

The <b>IWMPPlayer4</b> interface duplicates the methods of <b>IWMPPlayer</b>, <b>IWMPPlayer2</b>, and <b>IWMPPlayer3</b>, inherits the methods of <b>IWMPCore3</b>, and exposes the following additional methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayer4</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPPlayer4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayer4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563523(v=VS.85).aspx">get_isRemote</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control is running in remote mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563524(v=VS.85).aspx">get_playerApplication</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlayerApplication</b> interface when a remoted Windows Media Player control is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563525(v=VS.85).aspx">openPlayer</a>
</td>
<td align="left" width="63%">
Opens Windows Media Player using the specified URL.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayer4</b> interface either by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/en-us/library/Dd563514(v=VS.85).aspx">IWMPPlayer</a> interface or by calling the COM <b>CoCreateInstance</b> method.

	


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563217(v=VS.85).aspx">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563219(v=VS.85).aspx">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563514(v=VS.85).aspx">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563515(v=VS.85).aspx">IWMPPlayer2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563521(v=VS.85).aspx">IWMPPlayer3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563527(v=VS.85).aspx">IWMPPlayerApplication Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

