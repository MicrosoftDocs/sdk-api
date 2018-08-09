---
UID: NF:wmp.IWMPPlaylistCollection.getAll
title: IWMPPlaylistCollection::getAll
author: windows-sdk-content
description: The getAll method retrieves a pointer to an IWMPPlaylistArray interface representing all of the playlists in the library.
old-location: wmp\iwmpplaylistcollection_getall.htm
old-project: WMP
ms.assetid: 5ebd966f-5fee-4a8a-909e-5adcbdebab54
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPPlaylistCollection interface [Windows Media Player],getAll method, IWMPPlaylistCollection.getAll, IWMPPlaylistCollection::getAll, IWMPPlaylistCollectiongetAll, getAll, getAll method [Windows Media Player], getAll method [Windows Media Player],IWMPPlaylistCollection interface, wmp.iwmpplaylistcollection_getall, wmp/IWMPPlaylistCollection::getAll
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
 - IWMPPlaylistCollection.getAll
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPPlaylistCollection::getAll


## -description



The <b>getAll</b> method retrieves a pointer to an <b>IWMPPlaylistArray</b> interface representing all of the playlists in the library.




## -parameters




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



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/e6fb0ed1-cdc1-4792-98cb-2acf27bce5ce">IWMPPlaylistArray Interface</a>



<a href="https://msdn.microsoft.com/b6861651-f0c3-4b99-8c81-a8a8f8b47692">IWMPPlaylistCollection Interface</a>
 

 

