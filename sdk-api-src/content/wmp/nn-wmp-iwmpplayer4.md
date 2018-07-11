---
UID: NN:wmp.IWMPPlayer4
title: IWMPPlayer4
author: windows-sdk-content
description: The IWMPPlayer4 interface provides methods for modifying the basic behavior of the Windows Media Player control user interface.
old-location: wmp\iwmpplayer4.htm
old-project: WMP
ms.assetid: afe5dbd1-96e1-4abe-b843-ec6130fa02d0
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPPlayer4, IWMPPlayer4 interface [Windows Media Player], IWMPPlayer4 interface [Windows Media Player],described, IWMPPlayer4Interface, wmp.iwmpplayer4, wmp/IWMPPlayer4
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
 - IWMPPlayer4
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/0b4f76f2-f62a-4c91-bbc4-166c450608dd">get_isRemote</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control is running in remote mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37b4b0b1-f16e-42ed-830e-9b0468a66eeb">get_playerApplication</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlayerApplication</b> interface when a remoted Windows Media Player control is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2f08758-cd72-4b6b-bc9c-86f93d1d76c2">openPlayer</a>
</td>
<td align="left" width="63%">
Opens Windows Media Player using the specified URL.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPPlayer4</b> interface either by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer</a> interface or by calling the COM <b>CoCreateInstance</b> method.

	


## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/5f839bfe-bf67-49eb-8743-57713e1be7c5">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/3004551e-ce36-4f15-88c3-93b2bfaa72fc">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/bf51d54d-d0aa-42ad-8180-d1f6487baac8">IWMPPlayer2 Interface</a>



<a href="https://msdn.microsoft.com/0d8a9414-5c5c-40e0-a34c-430ead01ef26">IWMPPlayer3 Interface</a>



<a href="https://msdn.microsoft.com/bcdd7ea9-66b2-40e9-89a1-0fec073ccd92">IWMPPlayerApplication Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

