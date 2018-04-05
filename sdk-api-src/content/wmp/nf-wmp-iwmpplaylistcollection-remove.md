---
UID: NF:wmp.IWMPPlaylistCollection.remove
title: IWMPPlaylistCollection::remove method
author: windows-driver-content
description: The remove method removes a playlist from the library.
old-location: wmp\iwmpplaylistcollection_remove.htm
old-project: WMP
ms.assetid: ed678c2c-bfde-424b-9c71-21270a32a08e
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPPlaylistCollection, IWMPPlaylistCollection interface [Windows Media Player], remove method, IWMPPlaylistCollection::remove, IWMPPlaylistCollectionremove, remove method [Windows Media Player], remove method [Windows Media Player], IWMPPlaylistCollection interface, remove,IWMPPlaylistCollection.remove, wmp.iwmpplaylistcollection_remove, wmp/IWMPPlaylistCollection::remove
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
-	IWMPPlaylistCollection.remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylistCollection::remove method


## -description



The <b>remove</b> method removes a playlist from the library.




## -parameters




### -param pItem [in]

Pointer to an <b>IWMPPlaylist</b> interface for the playlist that this method will remove.


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



Before calling this method, you must have full access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/b6861651-f0c3-4b99-8c81-a8a8f8b47692">IWMPPlaylistCollection Interface</a>
 

 

