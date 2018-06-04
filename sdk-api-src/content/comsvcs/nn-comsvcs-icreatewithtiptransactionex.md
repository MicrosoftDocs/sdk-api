---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ICreateWithTipTransactionEx interface


## -description


<p class="CCE_Message">[The TIP service feature are deprecated and might not be available in future versions of the operating system. Consider using the WS-AtomicTransaction (WS-AT) protocol as a replacement transaction coordination and propagation technology. For more information about WS-AT support in the .Net Framework, see <a href="http://go.microsoft.com/fwlink/p/?linkid=105715">Transactions</a>.]

Creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateWithTipTransactionEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreateWithTipTransactionEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateWithTipTransactionEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f0572eb-8633-4dc3-a013-9cf859241cd7">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a COM+ object that executes within the scope of the manual transaction specified by a TIP transaction URL.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/39b455d3-d3d2-46ae-a45e-b036c18e45bc">ICreateWithTransactionEx</a>
 

 

