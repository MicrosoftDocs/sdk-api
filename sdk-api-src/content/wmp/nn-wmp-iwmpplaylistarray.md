---
UID: NN:wmp.IWMPPlaylistArray
title: IWMPPlaylistArray
author: windows-sdk-content
description: The IWMPPlaylistArray interface provides methods for accessing a collection of IWMPPlaylist interface pointers by index number.
old-location: wmp\iwmpplaylistarray.htm
old-project: WMP
ms.assetid: e6fb0ed1-cdc1-4792-98cb-2acf27bce5ce
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPPlaylistArray, IWMPPlaylistArray interface [Windows Media Player], IWMPPlaylistArray interface [Windows Media Player],described, IWMPPlaylistArrayInterface, wmp.iwmpplaylistarray, wmp/IWMPPlaylistArray
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
 - IWMPPlaylistArray
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylistArray interface


## -description



The <b>IWMPPlaylistArray</b> interface provides methods for accessing a collection of <b>IWMPPlaylist</b> interface pointers by index number.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlaylistArray</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPPlaylistArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlaylistArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ce0058c-8839-43da-aad8-4bc423ff3cde">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the number of playlists in the playlist array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IWMPPlaylist</b> interface representing the playlist at the specified index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

