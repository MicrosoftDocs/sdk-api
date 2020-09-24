---
UID: NF:wmp.IWMPPlaylistCollection.getByName
title: IWMPPlaylistCollection::getByName (wmp.h)
description: The getByName method retrieves a pointer to an IWMPPlaylistArray interface on an object containing playlists with the specified name, if any exist.
helpviewer_keywords: ["IWMPPlaylistCollection interface [Windows Media Player]","getByName method","IWMPPlaylistCollection.getByName","IWMPPlaylistCollection::getByName","IWMPPlaylistCollectiongetByName","getByName","getByName method [Windows Media Player]","getByName method [Windows Media Player]","IWMPPlaylistCollection interface","wmp.iwmpplaylistcollection_getbyname","wmp/IWMPPlaylistCollection::getByName"]
old-location: wmp\iwmpplaylistcollection_getbyname.htm
tech.root: WMP
ms.assetid: 9d837c57-8612-47ef-a0fa-a3ffa77ac704
ms.date: 12/05/2018
ms.keywords: IWMPPlaylistCollection interface [Windows Media Player],getByName method, IWMPPlaylistCollection.getByName, IWMPPlaylistCollection::getByName, IWMPPlaylistCollectiongetByName, getByName, getByName method [Windows Media Player], getByName method [Windows Media Player],IWMPPlaylistCollection interface, wmp.iwmpplaylistcollection_getbyname, wmp/IWMPPlaylistCollection::getByName
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
 - IWMPPlaylistCollection::getByName
 - wmp/IWMPPlaylistCollection::getByName
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
 - IWMPPlaylistCollection.getByName
---

# IWMPPlaylistCollection::getByName


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

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-get_count">IWMPPlaylistArray::get_count</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection">IWMPPlaylistCollection Interface</a>