---
UID: NN:wmp.IWMPPlaylist
title: IWMPPlaylist
author: windows-driver-content
description: The IWMPPlaylist interface provides methods for manipulating lists of media items.
old-location: wmp\iwmpplaylist.htm
old-project: WMP
ms.assetid: 04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPPlaylist, IWMPPlaylist interface [Windows Media Player], IWMPPlaylist interface [Windows Media Player], described, IWMPPlaylistInterface, wmp.iwmpplaylist, wmp/IWMPPlaylist
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
-	IWMPPlaylist
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylist interface


## -description



The <b>IWMPPlaylist</b> interface provides methods for manipulating lists of media items.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlaylist</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPPlaylist</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlaylist</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6db41d8-a4d5-4cab-9612-0562f3e92c25">appendItem</a>
</td>
<td align="left" width="63%">
Adds a media item to the end of the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">clear</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32c18feb-4df2-41d6-9adf-49836b6b836d">get_attributeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes associated with the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30bdf1e0-2bb8-486e-bec7-d06e1ac6ed9b">get_attributeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of an attribute specified by an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e37d1d96-27c3-415a-ac85-ab4b94dbc688">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/480fa108-5cfd-49ab-92fe-c635f13f3194">get_isIdentical</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified playlist is identical to the current playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20da6e49-720c-4291-9fb7-def441c7fc66">get_item</a>
</td>
<td align="left" width="63%">
Retrieves the media item at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/547a8ebe-b7c7-4dbc-96c4-1d5f5ef77f97">get_name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6763274-01e4-4a2f-9467-150e1964193a">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves the value of a playlist attribute specified by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2db2d28d-4cbf-423c-824f-e1e212c46f7a">insertItem</a>
</td>
<td align="left" width="63%">
Adds a media item at the specified location in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f408c7a0-d1d6-4c0d-8ee5-0afd43b19a9d">moveItem</a>
</td>
<td align="left" width="63%">
Changes the location of a media item in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/749dae2f-d9c3-4bbb-9a2f-042388f5ce0c">put_name</a>
</td>
<td align="left" width="63%">
Specifies the name of the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a17b0e0-2eaf-4570-a297-c2540ae4b6c5">removeItem</a>
</td>
<td align="left" width="63%">
Removes the specified media item from the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd812af6-0bdf-4da4-a066-4411d0d9e259">setItemInfo</a>
</td>
<td align="left" width="63%">
Specifies the value of an attribute of the current playlist.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

