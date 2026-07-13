---
UID: NF:wmp.IWMPPlaylistCollection.isDeleted
title: IWMPPlaylistCollection::isDeleted (wmp.h)
description: The isDeleted method retrieves a value indicating whether the specified playlist is in the deleted items folder.
helpviewer_keywords: ["IWMPPlaylistCollection interface [Windows Media Player]","isDeleted method","IWMPPlaylistCollection.isDeleted","IWMPPlaylistCollection::isDeleted","IWMPPlaylistCollectionisDeleted","isDeleted","isDeleted method [Windows Media Player]","isDeleted method [Windows Media Player]","IWMPPlaylistCollection interface","wmp.iwmpplaylistcollection_isdeleted","wmp/IWMPPlaylistCollection::isDeleted"]
old-location: wmp\iwmpplaylistcollection_isdeleted.htm
tech.root: WMP
ms.assetid: ac3e3401-ac7e-44d2-9680-5abe69678fc7
ms.date: 4/26/2023
ms.keywords: IWMPPlaylistCollection interface [Windows Media Player],isDeleted method, IWMPPlaylistCollection.isDeleted, IWMPPlaylistCollection::isDeleted, IWMPPlaylistCollectionisDeleted, isDeleted, isDeleted method [Windows Media Player], isDeleted method [Windows Media Player],IWMPPlaylistCollection interface, wmp.iwmpplaylistcollection_isdeleted, wmp/IWMPPlaylistCollection::isDeleted
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
 - IWMPPlaylistCollection::isDeleted
 - wmp/IWMPPlaylistCollection::isDeleted
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
 - IWMPPlaylistCollection.isDeleted
---

# IWMPPlaylistCollection::isDeleted


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection">IWMPPlaylistCollection Interface</a>