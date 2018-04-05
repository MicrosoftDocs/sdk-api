---
UID: NF:wmp.IWMPMedia.isMemberOf
title: IWMPMedia::isMemberOf method
author: windows-driver-content
description: The isMemberOf method retrieves a value indicating whether the specified media item is a member of the specified playlist.
old-location: wmp\iwmpmedia_ismemberof.htm
old-project: WMP
ms.assetid: 5ca46263-1e8e-42db-a131-e7534f79ca8e
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPMedia, IWMPMedia interface [Windows Media Player], isMemberOf method, IWMPMedia2 interface [Windows Media Player], isMemberOf method, IWMPMedia2::isMemberOf, IWMPMedia3 interface [Windows Media Player], isMemberOf method, IWMPMedia3::isMemberOf, IWMPMedia::isMemberOf, IWMPMediaisMemberOf, isMemberOf method [Windows Media Player], isMemberOf method [Windows Media Player], IWMPMedia interface, isMemberOf method [Windows Media Player], IWMPMedia2 interface, isMemberOf method [Windows Media Player], IWMPMedia3 interface, isMemberOf,IWMPMedia.isMemberOf, wmp.iwmpmedia_ismemberof, wmp/IWMPMedia2::isMemberOf, wmp/IWMPMedia3::isMemberOf, wmp/IWMPMedia::isMemberOf
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
-	IWMPMedia.isMemberOf
-	IWMPMedia2.isMemberOf
-	IWMPMedia3.isMemberOf
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia::isMemberOf method


## -description



The <b>isMemberOf</b> method retrieves a value indicating whether the specified media item is a member of the specified playlist.




## -parameters




### -param pPlaylist [in]

Pointer to an <b>IWMPPlaylist</b> interface.


### -param pvarfIsMemberOf [out]

Pointer to a <b>VARIANT_BOOL</b> that indicates whether the item is a member of the playlist.


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



This method cannot check playlists retrieved through the <b>MediaCollection</b> object. To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the <b>IWMPCore::get_playlistCollection</b> method. Once you retrieve the collection, retrieve the individual playlist by calling the <b>IWMPPlaylistCollection::getByName</b> method.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/8f6ab34f-e055-4a18-b1b8-e3c7b8f9c76a">IWMPCore::get_playlistCollection</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/9d837c57-8612-47ef-a0fa-a3ffa77ac704">IWMPPlaylistCollection::getByName</a>
 

 

