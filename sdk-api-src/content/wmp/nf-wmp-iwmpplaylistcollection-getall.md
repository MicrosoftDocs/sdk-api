---
UID: NF:wmp.IWMPPlaylistCollection.getAll
title: IWMPPlaylistCollection::getAll (wmp.h)
description: The getAll method retrieves a pointer to an IWMPPlaylistArray interface representing all of the playlists in the library.
helpviewer_keywords: ["IWMPPlaylistCollection interface [Windows Media Player]","getAll method","IWMPPlaylistCollection.getAll","IWMPPlaylistCollection::getAll","IWMPPlaylistCollectiongetAll","getAll","getAll method [Windows Media Player]","getAll method [Windows Media Player]","IWMPPlaylistCollection interface","wmp.iwmpplaylistcollection_getall","wmp/IWMPPlaylistCollection::getAll"]
old-location: wmp\iwmpplaylistcollection_getall.htm
tech.root: WMP
ms.assetid: 5ebd966f-5fee-4a8a-909e-5adcbdebab54
ms.date: 12/05/2018
ms.keywords: IWMPPlaylistCollection interface [Windows Media Player],getAll method, IWMPPlaylistCollection.getAll, IWMPPlaylistCollection::getAll, IWMPPlaylistCollectiongetAll, getAll, getAll method [Windows Media Player], getAll method [Windows Media Player],IWMPPlaylistCollection interface, wmp.iwmpplaylistcollection_getall, wmp/IWMPPlaylistCollection::getAll
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
 - IWMPPlaylistCollection::getAll
 - wmp/IWMPPlaylistCollection::getAll
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
 - IWMPPlaylistCollection.getAll
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

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray">IWMPPlaylistArray Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection">IWMPPlaylistCollection Interface</a>