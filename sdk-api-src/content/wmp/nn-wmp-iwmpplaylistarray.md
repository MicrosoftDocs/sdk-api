---
UID: NN:wmp.IWMPPlaylistArray
title: IWMPPlaylistArray (wmp.h)
description: The IWMPPlaylistArray interface provides methods for accessing a collection of IWMPPlaylist interface pointers by index number.
old-location: wmp\iwmpplaylistarray.htm
tech.root: WMP
ms.assetid: e6fb0ed1-cdc1-4792-98cb-2acf27bce5ce
ms.date: 12/05/2018
ms.keywords: IWMPPlaylistArray, IWMPPlaylistArray interface [Windows Media Player], IWMPPlaylistArray interface [Windows Media Player],described, IWMPPlaylistArrayInterface, wmp.iwmpplaylistarray, wmp/IWMPPlaylistArray
ms.topic: interface
f1_keywords:
- wmp/IWMPPlaylistArray
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
- IWMPPlaylistArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlaylistArray interface


## -description



The <b>IWMPPlaylistArray</b> interface provides methods for accessing a collection of <b>IWMPPlaylist</b> interface pointers by index number.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlaylistArray</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPPlaylistArray</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-get_count">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the number of playlists in the playlist array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item">item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IWMPPlaylist</b> interface representing the playlist at the specified index.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

