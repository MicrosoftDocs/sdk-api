---
UID: NF:wmp.IWMPMediaCollection.getByAlbum
title: IWMPMediaCollection::getByAlbum
author: windows-sdk-content
description: The getByAlbum method retrieves a pointer to an IWMPPlaylist interface. This interface contains the media items from the specified album.
old-location: wmp\iwmpmediacollection_getbyalbum.htm
tech.root: WMP
ms.assetid: 8db2349b-46f4-4863-a409-a85983362046
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getByAlbum method, IWMPMediaCollection.getByAlbum, IWMPMediaCollection::getByAlbum, IWMPMediaCollectiongetByAlbum, getByAlbum, getByAlbum method [Windows Media Player], getByAlbum method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getbyalbum, wmp/IWMPMediaCollection::getByAlbum
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
 - IWMPMediaCollection.getByAlbum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMediaCollection::getByAlbum


## -description



The <b>getByAlbum</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface contains the media items from the specified album.




## -parameters




### -param bstrAlbum [in]

String containing the album.


### -param ppMediaItems [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the retrieved media items.


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

There are two ways you ways you can retrieve an <b>IWMPMediaCollection</b> interface, and the behavior of the <b>getByAlbum</b> method depends on which of those two ways you use. If you retrieve the interface by calling <a href="https://msdn.microsoft.com/en-us/library/Dd563231(v=VS.85).aspx">IWMPCore::get_mediaCollection</a>, then the <b>getByAlbum</b> method returns all the media items in the library that belong to the specified album. If you retrieve the interface by calling <a href="https://msdn.microsoft.com/en-us/library/Dd563392(v=VS.85).aspx">IWMPLibrary::get_mediaCollection</a>, then the <b>getByAlbum</b> method returns only the audio items in the library that belong to the specified album.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563405(v=VS.85).aspx">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563547(v=VS.85).aspx">IWMPPlaylist Interface</a>
 

 

