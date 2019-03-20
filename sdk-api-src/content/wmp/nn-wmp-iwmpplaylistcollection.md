---
UID: NN:wmp.IWMPPlaylistCollection
title: IWMPPlaylistCollection (wmp.h)
author: windows-sdk-content
description: The IWMPPlaylistCollection interface provides methods for manipulating the IWMPPlaylist and IWMPPlaylistArray interfaces.
old-location: wmp\iwmpplaylistcollection.htm
tech.root: WMP
ms.assetid: b6861651-f0c3-4b99-8c81-a8a8f8b47692
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPlaylistCollection, IWMPPlaylistCollection interface [Windows Media Player], IWMPPlaylistCollection interface [Windows Media Player],described, IWMPPlaylistCollectionInterface, wmp.iwmpplaylistcollection, wmp/IWMPPlaylistCollection
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
 - IWMPPlaylistCollection
 - IWMPPlaylistCollection.setDeleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlaylistCollection interface


## -description



The <b>IWMPPlaylistCollection</b> interface provides methods for manipulating the <b>IWMPPlaylist</b> and <b>IWMPPlaylistArray</b> interfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlaylistCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPPlaylistCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlaylistCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563553(v=VS.85).aspx">getAll</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylistArray</b> interface on an object containing all of the playlists in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563554(v=VS.85).aspx">getByName</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylistArray</b> interface on an object containing playlists with the specified name, if any exist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563556(v=VS.85).aspx">importPlaylist</a>
</td>
<td align="left" width="63%">
Adds a static playlist to the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563557(v=VS.85).aspx">isDeleted</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified playlist is in the deleted items folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563558(v=VS.85).aspx">newPlaylist</a>
</td>
<td align="left" width="63%">
Creates a new, empty playlist in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563559(v=VS.85).aspx">remove</a>
</td>
<td align="left" width="63%">
Removes a playlist from the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>setDeleted</b></td>
<td align="left" width="63%">
No longer supported.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563547(v=VS.85).aspx">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563548(v=VS.85).aspx">IWMPPlaylistArray Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

