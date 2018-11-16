---
UID: NN:wmp.IWMPPlaylistCollection
title: IWMPPlaylistCollection
author: windows-sdk-content
description: The IWMPPlaylistCollection interface provides methods for manipulating the IWMPPlaylist and IWMPPlaylistArray interfaces.
old-location: wmp\iwmpplaylistcollection.htm
tech.root: WMP
ms.assetid: b6861651-f0c3-4b99-8c81-a8a8f8b47692
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPPlaylistCollection, IWMPPlaylistCollection interface [Windows Media Player], IWMPPlaylistCollection interface [Windows Media Player],described, IWMPPlaylistCollectionInterface, wmp.iwmpplaylistcollection, wmp/IWMPPlaylistCollection
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlaylistCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPPlaylistCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5ebd966f-5fee-4a8a-909e-5adcbdebab54">getAll</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylistArray</b> interface on an object containing all of the playlists in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d837c57-8612-47ef-a0fa-a3ffa77ac704">getByName</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylistArray</b> interface on an object containing playlists with the specified name, if any exist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/421a1bd3-65c1-4d8f-be75-918b1cfa06d2">importPlaylist</a>
</td>
<td align="left" width="63%">
Adds a static playlist to the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac3e3401-ac7e-44d2-9680-5abe69678fc7">isDeleted</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified playlist is in the deleted items folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ad51469-a150-4322-ac16-782ef0d96a57">newPlaylist</a>
</td>
<td align="left" width="63%">
Creates a new, empty playlist in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed678c2c-bfde-424b-9c71-21270a32a08e">remove</a>
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




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/e6fb0ed1-cdc1-4792-98cb-2acf27bce5ce">IWMPPlaylistArray Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

