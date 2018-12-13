---
UID: NF:wmp.IWMPPlaylist.removeItem
title: IWMPPlaylist::removeItem
author: windows-sdk-content
description: The removeItem method removes the specified media item from the playlist.
old-location: wmp\iwmpplaylist_removeitem.htm
tech.root: WMP
ms.assetid: 7a17b0e0-2eaf-4570-a297-c2540ae4b6c5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPPlaylist interface [Windows Media Player],removeItem method, IWMPPlaylist.removeItem, IWMPPlaylist::removeItem, IWMPPlaylistremoveItem, removeItem, removeItem method [Windows Media Player], removeItem method [Windows Media Player],IWMPPlaylist interface, wmp.iwmpplaylist_removeitem, wmp/IWMPPlaylist::removeItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPPlaylist.removeItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlaylist::removeItem


## -description



The <b>removeItem</b> method removes the specified media item from the playlist.




## -parameters




### -param pIWMPMedia [in]

Pointer to an <b>IWMPMedia</b> interface for the item to remove.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.

If there is no next item, the previous item is used. If there are no other items, then the <b>IWMPCore::get_currentMedia</b> method will return <b>NULL</b>.

Before calling this method, you must have full access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/4f199336-0555-40de-8d27-780b05ef9510">IWMPCore::get_currentMedia</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/2db2d28d-4cbf-423c-824f-e1e212c46f7a">IWMPPlaylist::insertItem</a>
 

 

