---
UID: NF:wmp.IWMPPlaylistCollection.getByName
title: IWMPPlaylistCollection::getByName method
author: windows-driver-content
description: The getByName method retrieves a pointer to an IWMPPlaylistArray interface on an object containing playlists with the specified name, if any exist.
old-location: wmp\iwmpplaylistcollection_getbyname.htm
old-project: WMP
ms.assetid: 9d837c57-8612-47ef-a0fa-a3ffa77ac704
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPPlaylistCollection, IWMPPlaylistCollection interface [Windows Media Player], getByName method, IWMPPlaylistCollection::getByName, IWMPPlaylistCollectiongetByName, getByName method [Windows Media Player], getByName method [Windows Media Player], IWMPPlaylistCollection interface, getByName,IWMPPlaylistCollection.getByName, wmp.iwmpplaylistcollection_getbyname, wmp/IWMPPlaylistCollection::getByName
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
-	IWMPPlaylistCollection.getByName
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylistCollection::getByName method


## -description



The <b>getByName</b> method retrieves a pointer to an <b>IWMPPlaylistArray</b> interface on an object containing playlists with the specified name, if any exist.




## -parameters




### -param bstrName [in]

String containing the name.


### -param ppPlaylistArray [out]

Pointer to a pointer to an <b>IWMPPlaylistArray</b> interface for the retrieved array of playlists.


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



Use <b>IWMPPlaylistArray::count</b> to determine whether a playlist exists. If <b>count</b> is zero, the array is empty.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/2ce0058c-8839-43da-aad8-4bc423ff3cde">IWMPPlaylistArray::get_count</a>



<a href="https://msdn.microsoft.com/b6861651-f0c3-4b99-8c81-a8a8f8b47692">IWMPPlaylistCollection Interface</a>
 

 

