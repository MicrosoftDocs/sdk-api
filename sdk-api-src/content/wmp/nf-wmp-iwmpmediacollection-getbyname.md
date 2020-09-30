---
UID: NF:wmp.IWMPMediaCollection.getByName
title: IWMPMediaCollection::getByName (wmp.h)
description: The getByName method retrieves a pointer to an IWMPPlaylist interface. This interface contains the media items with the specified name.
helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","getByName method","IWMPMediaCollection.getByName","IWMPMediaCollection::getByName","IWMPMediaCollectiongetByName","getByName","getByName method [Windows Media Player]","getByName method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_getbyname","wmp/IWMPMediaCollection::getByName"]
old-location: wmp\iwmpmediacollection_getbyname.htm
tech.root: WMP
ms.assetid: 114b0449-a45e-42e5-9e68-428c40a388cf
ms.date: 12/05/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getByName method, IWMPMediaCollection.getByName, IWMPMediaCollection::getByName, IWMPMediaCollectiongetByName, getByName, getByName method [Windows Media Player], getByName method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getbyname, wmp/IWMPMediaCollection::getByName
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
 - IWMPMediaCollection::getByName
 - wmp/IWMPMediaCollection::getByName
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
 - IWMPMediaCollection.getByName
---

# IWMPMediaCollection::getByName


## -description

The <b>getByName</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface contains the media items with the specified name.

## -parameters

### -param bstrName [in]

String containing the specified name.

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

There are two ways you ways you can retrieve an <b>IWMPMediaCollection</b> interface, and the behavior of the <b>getByName</b> method depends on which of those two ways you use. If you retrieve the interface by calling <a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection">IWMPCore::get_mediaCollection</a>, then the <b>getByName</b> method returns all the media items in the library that have the specified name. If you retrieve the interface by calling <a href="/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection">IWMPLibrary::get_mediaCollection</a>, then the <b>getByName</b> method returns only the audio items in the library that have the specified name.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>