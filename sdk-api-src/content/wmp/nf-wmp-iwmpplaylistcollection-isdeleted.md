---
UID: NF:wmp.IWMPPlaylistCollection.isDeleted
title: IWMPPlaylistCollection::isDeleted method
author: windows-driver-content
description: The isDeleted method retrieves a value indicating whether the specified playlist is in the deleted items folder.
old-location: wmp\iwmpplaylistcollection_isdeleted.htm
old-project: WMP
ms.assetid: ac3e3401-ac7e-44d2-9680-5abe69678fc7
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPPlaylistCollection, IWMPPlaylistCollection interface [Windows Media Player], isDeleted method, IWMPPlaylistCollection::isDeleted, IWMPPlaylistCollectionisDeleted, isDeleted method [Windows Media Player], isDeleted method [Windows Media Player], IWMPPlaylistCollection interface, isDeleted,IWMPPlaylistCollection.isDeleted, wmp.iwmpplaylistcollection_isdeleted, wmp/IWMPPlaylistCollection::isDeleted
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
-	IWMPPlaylistCollection.isDeleted
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylistCollection::isDeleted method


## -description



The <b>isDeleted</b> method retrieves a value indicating whether the specified playlist is in the deleted items folder.




## -parameters




### -param pItem [in]

Pointer to an <b>IWMPPlaylist</b> interface for the queried playlist.


### -param pvarfIsDeleted [out]

Pointer to a <b>VARIANT_BOOL</b> that specifies whether the given playlist was deleted.


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



<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/b6861651-f0c3-4b99-8c81-a8a8f8b47692">IWMPPlaylistCollection Interface</a>
 

 

