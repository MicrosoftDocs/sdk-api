---
UID: NF:wmp.IWMPPlaylistCollection.newPlaylist
title: IWMPPlaylistCollection::newPlaylist
author: windows-sdk-content
description: The newPlaylist method creates a new, empty playlist in the library.
old-location: wmp\iwmpplaylistcollection_newplaylist.htm
old-project: WMP
ms.assetid: 5ad51469-a150-4322-ac16-782ef0d96a57
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlaylistCollection interface [Windows Media Player],newPlaylist method, IWMPPlaylistCollection.newPlaylist, IWMPPlaylistCollection::newPlaylist, IWMPPlaylistCollectionnewPlaylist, newPlaylist, newPlaylist method [Windows Media Player], newPlaylist method [Windows Media Player],IWMPPlaylistCollection interface, wmp.iwmpplaylistcollection_newplaylist, wmp/IWMPPlaylistCollection::newPlaylist
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPPlaylistCollection.newPlaylist
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylistCollection::newPlaylist


## -description



The <b>newPlaylist</b> method creates a new, empty playlist in the library.




## -parameters




### -param bstrName [in]

String containing the name of the new playlist.


### -param ppItem [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the new playlist.


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



This method creates an empty playlist in the library. To fill the playlist with media items, use <b>IWMPPlaylist::appendItem</b> or <b>IWMPPlaylist::insertItem</b>.

Multiple playlists having the same name are permitted in the library. To avoid creating a duplicate playlist name with this method, use the <b>getByName</b> method and <b>IWMPPlaylistArray::count</b> to determine whether a playlist with a particular name already exists.

Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the bstrName parameter.

Before calling this method, you must have full access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/e6db41d8-a4d5-4cab-9612-0562f3e92c25">IWMPPlaylist::appendItem</a>



<a href="https://msdn.microsoft.com/2db2d28d-4cbf-423c-824f-e1e212c46f7a">IWMPPlaylist::insertItem</a>



<a href="https://msdn.microsoft.com/2ce0058c-8839-43da-aad8-4bc423ff3cde">IWMPPlaylistArray::get_count</a>



<a href="https://msdn.microsoft.com/b6861651-f0c3-4b99-8c81-a8a8f8b47692">IWMPPlaylistCollection Interface</a>



<a href="https://msdn.microsoft.com/9d837c57-8612-47ef-a0fa-a3ffa77ac704">IWMPPlaylistCollection::getByName</a>
 

 

