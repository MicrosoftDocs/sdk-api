---
UID: NN:wmp.IWMPPlaylist
title: IWMPPlaylist (wmp.h)
description: The IWMPPlaylist interface provides methods for manipulating lists of media items.helpviewer_keywords: ["IWMPPlaylist","IWMPPlaylist interface [Windows Media Player]","IWMPPlaylist interface [Windows Media Player]","described","IWMPPlaylistInterface","wmp.iwmpplaylist","wmp/IWMPPlaylist"]
old-location: wmp\iwmpplaylist.htm
tech.root: WMP
ms.assetid: 04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9
ms.date: 12/05/2018
ms.keywords: IWMPPlaylist, IWMPPlaylist interface [Windows Media Player], IWMPPlaylist interface [Windows Media Player],described, IWMPPlaylistInterface, wmp.iwmpplaylist, wmp/IWMPPlaylist
f1_keywords:
- wmp/IWMPPlaylist
dev_langs:
- c++
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
- IWMPPlaylist
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlaylist interface


## -description



The <b>IWMPPlaylist</b> interface provides methods for manipulating lists of media items.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlaylist</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPPlaylist</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-appenditem">appendItem</a>
</td>
<td align="left" width="63%">
Adds a media item to the end of the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-clear">clear</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_attributecount">get_attributeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes associated with the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_attributename">get_attributeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of an attribute specified by an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_count">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_isidentical">get_isIdentical</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified playlist is identical to the current playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item">get_item</a>
</td>
<td align="left" width="63%">
Retrieves the media item at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_name">get_name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-getiteminfo">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves the value of a playlist attribute specified by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-insertitem">insertItem</a>
</td>
<td align="left" width="63%">
Adds a media item at the specified location in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem">moveItem</a>
</td>
<td align="left" width="63%">
Changes the location of a media item in the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-put_name">put_name</a>
</td>
<td align="left" width="63%">
Specifies the name of the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-removeitem">removeItem</a>
</td>
<td align="left" width="63%">
Removes the specified media item from the playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo">setItemInfo</a>
</td>
<td align="left" width="63%">
Specifies the value of an attribute of the current playlist.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

