---
UID: NF:wmp.IWMPMediaCollection.getByAuthor
title: IWMPMediaCollection::getByAuthor (wmp.h)
description: The getByAuthor method retrieves a pointer to an IWMPPlaylist interface. This interface contains the media items for the specified author.
helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","getByAuthor method","IWMPMediaCollection.getByAuthor","IWMPMediaCollection::getByAuthor","IWMPMediaCollectiongetByAuthor","getByAuthor","getByAuthor method [Windows Media Player]","getByAuthor method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_getbyauthor","wmp/IWMPMediaCollection::getByAuthor"]
old-location: wmp\iwmpmediacollection_getbyauthor.htm
tech.root: WMP
ms.assetid: 415dfbe5-c709-4674-bcdd-38742150d11f
ms.date: 12/05/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getByAuthor method, IWMPMediaCollection.getByAuthor, IWMPMediaCollection::getByAuthor, IWMPMediaCollectiongetByAuthor, getByAuthor, getByAuthor method [Windows Media Player], getByAuthor method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getbyauthor, wmp/IWMPMediaCollection::getByAuthor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPMediaCollection::getByAuthor
 - wmp/IWMPMediaCollection::getByAuthor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPMediaCollection.getByAuthor
---

# IWMPMediaCollection::getByAuthor


## -description

The <b>getByAuthor</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface contains the media items for the specified author.

## -parameters

### -param bstrAuthor [in]

String containing the specified author.

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

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

There are two ways you ways you can retrieve an <b>IWMPMediaCollection</b> interface, and the behavior of the <b>getByAuthor</b> method depends on which of those two ways you use. If you retrieve the interface by calling <a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection">IWMPCore::get_mediaCollection</a>, then the <b>getByAuthor</b> method returns all the media items in the library that have the specified author. If you retrieve the interface by calling <a href="/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection">IWMPLibrary::get_mediaCollection</a>, then the <b>getByAuthor</b> method returns only the audio items in the library that have the specified author.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>