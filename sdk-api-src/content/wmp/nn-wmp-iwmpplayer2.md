---
UID: NN:wmp.IWMPPlayer2
title: IWMPPlayer2 (wmp.h)
author: windows-sdk-content
description: The IWMPPlayer2 interface provides additional methods for modifying the basic behavior of the Windows Media Player control user interface.
old-location: wmp\iwmpplayer2.htm
tech.root: WMP
ms.assetid: bf51d54d-d0aa-42ad-8180-d1f6487baac8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPlayer2, IWMPPlayer2 interface [Windows Media Player], IWMPPlayer2 interface [Windows Media Player],described, IWMPPlayer2Interface, wmp.iwmpplayer2, wmp/IWMPPlayer2
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
 - IWMPPlayer2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563516(v=VS.85).aspx">get_stretchToFit</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video will stretch to fit size of the Windows Media Player control video display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563518(v=VS.85).aspx">get_windowlessVideo</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563519(v=VS.85).aspx">put_stretchToFit</a>
</td>
<td align="left" width="63%">
Specifies whether video will stretch to fit the size of the Windows Media Player control video display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563520(v=VS.85).aspx">put_windowlessVideo</a>
</td>
<td align="left" width="63%">
Specifies whether the Windows Media Player control renders video in windowless mode.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayer2</b> interface either by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/en-us/library/Dd563514(v=VS.85).aspx">IWMPPlayer</a> interface or by calling the COM <b>CoCreateInstance</b> method.

	


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563217(v=VS.85).aspx">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563219(v=VS.85).aspx">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563514(v=VS.85).aspx">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563521(v=VS.85).aspx">IWMPPlayer3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563522(v=VS.85).aspx">IWMPPlayer4 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

