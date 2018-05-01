---
UID: NF:wmp.IWMPPlaylistCollection.importPlaylist
title: IWMPPlaylistCollection::importPlaylist method
author: windows-driver-content
description: The importPlaylist method adds a static playlist to the library.
old-location: wmp\iwmpplaylistcollection_importplaylist.htm
old-project: WMP
ms.assetid: 421a1bd3-65c1-4d8f-be75-918b1cfa06d2
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPPlaylistCollection, IWMPPlaylistCollection interface [Windows Media Player], importPlaylist method, IWMPPlaylistCollection::importPlaylist, IWMPPlaylistCollectionimportPlaylist, importPlaylist method [Windows Media Player], importPlaylist method [Windows Media Player], IWMPPlaylistCollection interface, importPlaylist,IWMPPlaylistCollection.importPlaylist, wmp.iwmpplaylistcollection_importplaylist, wmp/IWMPPlaylistCollection::importPlaylist
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPPlaylistCollection.importPlaylist
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylistCollection::importPlaylist method


## -description



The <b>importPlaylist</b> method adds a static playlist to the library.




## -parameters




### -param pItem [in]

Pointer to an <b>IWMPPlaylist</b> interface for the playlist that this method will add.


### -param ppImportedItem [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the added playlist.


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



Playlists that do not contain any media items cannot be added to the library by using this method. To create an empty playlist in the library, use the <b>newPlaylist</b> method. You can then fill the resulting playlist with media items by using <b>IWMPPlaylist::appendItem</b> or <b>IWMPPlaylist::insertItem</b>.

If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist. To add an auto playlist to the library and preserve its automatic behavior, use <b>IWMPMediaCollection::add</b>. For more information, see <a href="https://msdn.microsoft.com/708c236e-8f3c-4188-aefb-eda7da598944">Static and Auto Playlists</a>.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/e6db41d8-a4d5-4cab-9612-0562f3e92c25">IWMPPlaylist::appendItem</a>



<a href="https://msdn.microsoft.com/2db2d28d-4cbf-423c-824f-e1e212c46f7a">IWMPPlaylist::insertItem</a>



<a href="https://msdn.microsoft.com/b6861651-f0c3-4b99-8c81-a8a8f8b47692">IWMPPlaylistCollection Interface</a>



<a href="https://msdn.microsoft.com/5ad51469-a150-4322-ac16-782ef0d96a57">IWMPPlaylistCollection::newPlaylist</a>
 

 

