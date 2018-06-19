---
UID: NN:wmp.IWMPStringCollection
title: IWMPStringCollection
author: windows-sdk-content
description: The IWMPStringCollection interface provides methods that work with a collection of strings.
old-location: wmp\iwmpstringcollection.htm
old-project: WMP
ms.assetid: 8cdabea9-7e37-4e63-9d6c-b6f63aa536ea
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPStringCollection, IWMPStringCollection interface [Windows Media Player], IWMPStringCollection interface [Windows Media Player],described, IWMPStringCollectionInterface, wmp.iwmpstringcollection, wmp/IWMPStringCollection
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
 - IWMPStringCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPStringCollection interface


## -description



The <b>IWMPStringCollection</b> interface provides methods that work with a collection of strings.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPStringCollection</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPStringCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPStringCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97865752-e4bf-4f91-b481-22d9c8b3e090">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the string collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">item</a>
</td>
<td align="left" width="63%">
Retrieves the string at the specified index.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPStringCollection</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection</a>
</td>
<td>
<a href="https://msdn.microsoft.com/c3699acb-58a1-4efa-a42c-c84534abca96">getAttributeStringCollection</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

