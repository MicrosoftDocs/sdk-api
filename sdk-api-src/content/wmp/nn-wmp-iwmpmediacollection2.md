---
UID: NN:wmp.IWMPMediaCollection2
title: IWMPMediaCollection2
author: windows-driver-content
description: The IWMPMediaCollection2 interface provides methods that supplement the IWMPMediaCollection interface.
old-location: wmp\iwmpmediacollection2.htm
old-project: WMP
ms.assetid: 576e231e-542a-495c-ad1b-a246339c3cb1
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPMediaCollection2, IWMPMediaCollection2 interface [Windows Media Player], IWMPMediaCollection2 interface [Windows Media Player], described, IWMPMediaCollection2Interface, wmp.iwmpmediacollection2, wmp/IWMPMediaCollection2
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPMediaCollection2
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMediaCollection2 interface


## -description



The <b>IWMPMediaCollection2</b> interface provides methods that supplement the <b>IWMPMediaCollection</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMediaCollection2</b> interface inherits from <a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection</a>. <b>IWMPMediaCollection2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPMediaCollection2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1e6bf08-3b81-4c04-92ff-73eac5f7495a">createQuery</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPQuery</b> interface that represents a new query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf925189-1f68-499c-9c98-063a0367dd3c">getByAttributeAndMediaType</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface that contains media items that have a specified attribute and media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3d4586b-c999-447c-b974-15bd0ef160a6">getPlaylistByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface that contains media items that match the query conditions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/070bc947-bf2b-4c06-9ffa-6a23625d178a">getStringCollectionByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPStringCollection</b> interface that contains the set of all string values for a specified attribute that match the query conditions.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

