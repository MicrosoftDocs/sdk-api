---
UID: NF:wmp.IWMPMediaCollection.getByAlbum
title: IWMPMediaCollection::getByAlbum (wmp.h)
description: The getByAlbum method retrieves a pointer to an IWMPPlaylist interface. This interface contains the media items from the specified album.helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","getByAlbum method","IWMPMediaCollection.getByAlbum","IWMPMediaCollection::getByAlbum","IWMPMediaCollectiongetByAlbum","getByAlbum","getByAlbum method [Windows Media Player]","getByAlbum method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_getbyalbum","wmp/IWMPMediaCollection::getByAlbum"]
old-location: wmp\iwmpmediacollection_getbyalbum.htm
tech.root: WMP
ms.assetid: 8db2349b-46f4-4863-a409-a85983362046
ms.date: 12/05/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getByAlbum method, IWMPMediaCollection.getByAlbum, IWMPMediaCollection::getByAlbum, IWMPMediaCollectiongetByAlbum, getByAlbum, getByAlbum method [Windows Media Player], getByAlbum method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getbyalbum, wmp/IWMPMediaCollection::getByAlbum
f1_keywords:
- wmp/IWMPMediaCollection.getByAlbum
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.

There are two ways you ways you can retrieve an <b>IWMPMediaCollection</b> interface, and the behavior of the <b>getByAlbum</b> method depends on which of those two ways you use. If you retrieve the interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection">IWMPCore::get_mediaCollection</a>, then the <b>getByAlbum</b> method returns all the media items in the library that belong to the specified album. If you retrieve the interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection">IWMPLibrary::get_mediaCollection</a>, then the <b>getByAlbum</b> method returns only the audio items in the library that belong to the specified album.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>
 

 

