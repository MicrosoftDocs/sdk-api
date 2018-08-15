---
UID: NN:wmp.IWMPPlayer2
title: IWMPPlayer2
author: windows-sdk-content
description: The IWMPPlayer2 interface provides additional methods for modifying the basic behavior of the Windows Media Player control user interface.
old-location: wmp\iwmpplayer2.htm
old-project: WMP
ms.assetid: bf51d54d-d0aa-42ad-8180-d1f6487baac8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlayer2, IWMPPlayer2 interface [Windows Media Player], IWMPPlayer2 interface [Windows Media Player],described, IWMPPlayer2Interface, wmp.iwmpplayer2, wmp/IWMPPlayer2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmp.h
req.include-header: 
req.redist: 
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
 - IWMPPlayer2
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlayer2 interface


## -description



The <b>IWMPPlayer2</b> interface provides additional methods for modifying the basic behavior of the Windows Media Player control user interface. These methods also supplement the <b>IWMPCore</b> interface.

The <b>IWMPPlayer2</b> interface duplicates the methods of <b>IWMPPlayer</b>, inherits the methods of <b>IWMPCore</b>, and exposes the following additional methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayer2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPPlayer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d477800d-fb16-49a7-ab80-a0f5f7c68fc7">get_stretchToFit</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video will stretch to fit size of the Windows Media Player control video display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da1cfa7c-aa79-4711-8de2-d83317e5598f">get_windowlessVideo</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1da60976-5f84-4dc7-8186-32f6d3bb9165">put_stretchToFit</a>
</td>
<td align="left" width="63%">
Specifies whether video will stretch to fit the size of the Windows Media Player control video display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/736eaf52-29bd-4223-a62d-d3d75cef1863">put_windowlessVideo</a>
</td>
<td align="left" width="63%">
Specifies whether the Windows Media Player control renders video in windowless mode.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayer2</b> interface either by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer</a> interface or by calling the COM <b>CoCreateInstance</b> method.

	


## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/5f839bfe-bf67-49eb-8743-57713e1be7c5">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/3004551e-ce36-4f15-88c3-93b2bfaa72fc">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/0d8a9414-5c5c-40e0-a34c-430ead01ef26">IWMPPlayer3 Interface</a>



<a href="https://msdn.microsoft.com/afe5dbd1-96e1-4abe-b843-ec6130fa02d0">IWMPPlayer4 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

