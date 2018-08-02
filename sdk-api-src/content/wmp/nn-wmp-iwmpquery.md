---
UID: NN:wmp.IWMPQuery
title: IWMPQuery
author: windows-sdk-content
description: The IWMPQuery interface represents a compound query.
old-location: wmp\iwmpquery.htm
old-project: WMP
ms.assetid: f1f3c46f-4756-49b4-ad4f-a9097ff787f8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPQuery, IWMPQuery interface [Windows Media Player], IWMPQuery interface [Windows Media Player],described, IWMPQueryInterface, wmp.iwmpquery, wmp/IWMPQuery
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
 - IWMPQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPQuery interface


## -description



The <b>IWMPQuery</b> interface represents a compound query.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPQuery</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d60474ce-a785-40b1-a4fb-80dc22fddedb">addCondition</a>
</td>
<td align="left" width="63%">
Adds a condition to the compound query using AND logic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c81a8125-2cfa-40e2-afc5-672c2866b880">beginNextGroup</a>
</td>
<td align="left" width="63%">
Begins a new condition group.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b1e6bf08-3b81-4c04-92ff-73eac5f7495a">IWMPMediaCollection2::createQuery</a>



<a href="https://msdn.microsoft.com/b3d4586b-c999-447c-b974-15bd0ef160a6">IWMPMediaCollection2::getPlaylistByQuery</a>



<a href="https://msdn.microsoft.com/070bc947-bf2b-4c06-9ffa-6a23625d178a">IWMPMediaCollection2::getStringCollectionByQuery</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

