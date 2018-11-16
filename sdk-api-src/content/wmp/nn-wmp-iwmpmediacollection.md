---
UID: NN:wmp.IWMPMediaCollection
title: IWMPMediaCollection
author: windows-sdk-content
description: The IWMPMediaCollection interface provides methods that can be used to organize a large collection of media items.
old-location: wmp\iwmpmediacollection.htm
tech.root: WMP
ms.assetid: bf975a30-dfb1-4994-9095-510a6b997aff
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPMediaCollection, IWMPMediaCollection interface [Windows Media Player], IWMPMediaCollection interface [Windows Media Player],described, IWMPMediaCollectionInterface, wmp.iwmpmediacollection, wmp/IWMPMediaCollection
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
 - IWMPMediaCollection
 - IWMPMediaCollection.isDeleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMediaCollection interface


## -description



The <b>IWMPMediaCollection</b> interface provides methods that can be used to organize a large collection of media items.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMediaCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPMediaCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPMediaCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9dfefbc-c240-41c0-abb9-4bc5012c147c">add</a>
</td>
<td align="left" width="63%">
Adds a new media item to the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db06194c-36e2-4494-b464-c08f6983bdc1">getAll</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface that corresponds to the playlist that contains all media items in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3699acb-58a1-4efa-a42c-c84534abca96">getAttributeStringCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPStringCollection</b> interface that represents the set of all values for a given attribute within a given media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8db2349b-46f4-4863-a409-a85983362046">getByAlbum</a>
</td>
<td align="left" width="63%">
Retries a pointer to an <b>IWMPPlaylist</b> interface to an object containing media items from the specified album.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab1c53dd-6145-4b2b-a665-4c8c79143284">getByAttribute</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface that corresponds to the specified attribute having the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/415dfbe5-c709-4674-bcdd-38742150d11f">getByAuthor</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface that contains the media items for the specified author.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/292189a5-06ec-4870-b279-5190c57c77c9">getByGenre</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface to an object containing media items with the specified genre.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/114b0449-a45e-42e5-9e68-428c40a388cf">getByName</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface that contains the media items with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22024108-398e-4a05-b5ed-311583c69497">getMediaAtom</a>
</td>
<td align="left" width="63%">
Retrieves the index at which a given attribute resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>isDeleted</b></td>
<td align="left" width="63%">
No longer supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/646d2e3c-623b-4040-af82-1cefac6fc1ae">remove</a>
</td>
<td align="left" width="63%">
Removes the specified media item from the media collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bba1e7a-3c1f-4f69-b4ab-68a9cf3b97d0">setDeleted</a>
</td>
<td align="left" width="63%">
Moves the specified media item to the deleted items folder.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

