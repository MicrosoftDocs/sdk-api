---
UID: NF:wmp.IWMPMediaCollection2.getPlaylistByQuery
title: IWMPMediaCollection2::getPlaylistByQuery (wmp.h)
description: The getPlaylistByQuery method retrieves a pointer to an IWMPPlaylist interface. This interface represents a playlist that contains media items that match the query conditions.
helpviewer_keywords: ["IWMPMediaCollection2 interface [Windows Media Player]","getPlaylistByQuery method","IWMPMediaCollection2.getPlaylistByQuery","IWMPMediaCollection2::getPlaylistByQuery","IWMPMediaCollection2getPlaylistByQuery","getPlaylistByQuery","getPlaylistByQuery method [Windows Media Player]","getPlaylistByQuery method [Windows Media Player]","IWMPMediaCollection2 interface","wmp.iwmpmediacollection2_getplaylistbyquery","wmp/IWMPMediaCollection2::getPlaylistByQuery"]
old-location: wmp\iwmpmediacollection2_getplaylistbyquery.htm
tech.root: WMP
ms.assetid: b3d4586b-c999-447c-b974-15bd0ef160a6
ms.date: 4/26/2023
ms.keywords: IWMPMediaCollection2 interface [Windows Media Player],getPlaylistByQuery method, IWMPMediaCollection2.getPlaylistByQuery, IWMPMediaCollection2::getPlaylistByQuery, IWMPMediaCollection2getPlaylistByQuery, getPlaylistByQuery, getPlaylistByQuery method [Windows Media Player], getPlaylistByQuery method [Windows Media Player],IWMPMediaCollection2 interface, wmp.iwmpmediacollection2_getplaylistbyquery, wmp/IWMPMediaCollection2::getPlaylistByQuery
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPMediaCollection2::getPlaylistByQuery
 - wmp/IWMPMediaCollection2::getPlaylistByQuery
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
 - IWMPMediaCollection2.getPlaylistByQuery
---

# IWMPMediaCollection2::getPlaylistByQuery


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getPlaylistByQuery</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface represents a playlist that contains media items that match the query conditions.

## -parameters

### -param pQuery [in]

Pointer to the <b>IWMPQuery</b> interface that represents the query.

### -param bstrMediaType [in]

String that contains the media type. Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".

### -param bstrSortAttribute [in]

String that contains the attribute name used for sorting. An empty string means that no sorting is applied.

### -param fSortAscending [in]

<b>VARIANT_BOOL</b> that indicates whether the playlist must be sorted in ascending order.

### -param ppPlaylist [out]

Address of a variable that receives a pointer to an <b>IWMPPlaylist</b> interface for the retrieved playlist.

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

Compound queries using <b>IWMPQuery</b> are not case sensitive.

When the compound query specified by the <i>pQuery</i> parameter contains a condition built on the <b>MediaType</b> attribute, that condition is ignored. The value for the <i>bstrMediaType</i> parameter is always used. For example, if the compound query contains the condition "MediaType Equals audio" and the value for the <i>bstrMediaType</i> parameter is "video", the resulting playlist will contain only video items.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2">IWMPMediaCollection2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpquery">IWMPQuery Interface</a>



<a href="/windows/desktop/WMP/mediatype-attribute">MediaType Attribute</a>