---
UID: NF:wmp.IWMPMediaCollection.add
title: IWMPMediaCollection::add (wmp.h)
description: The add method adds a new media item or playlist to the library.
helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","add method","IWMPMediaCollection.add","IWMPMediaCollection::add","IWMPMediaCollectionadd","add","add method [Windows Media Player]","add method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_add","wmp/IWMPMediaCollection::add"]
old-location: wmp\iwmpmediacollection_add.htm
tech.root: WMP
ms.assetid: f9dfefbc-c240-41c0-abb9-4bc5012c147c
ms.date: 4/26/2023
ms.keywords: IWMPMediaCollection interface [Windows Media Player],add method, IWMPMediaCollection.add, IWMPMediaCollection::add, IWMPMediaCollectionadd, add, add method [Windows Media Player], add method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_add, wmp/IWMPMediaCollection::add
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
 - IWMPMediaCollection::add
 - wmp/IWMPMediaCollection::add
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
 - IWMPMediaCollection.add
---

# IWMPMediaCollection::add


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>add</b> method adds a new media item or playlist to the library.

## -parameters

### -param bstrURL [in]

String containing the URL that specifies the location of the media item or playlist.

### -param ppItem [out]

Pointer to a pointer to the <b>IWMPMedia</b> interface for the added item or playlist.

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

This method loads an existing media item or playlist into the library, given a path. This method does not move or change the file. This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.

This method accepts both static and auto playlist files. The <b>IWMPPlaylistCollection::importPlaylist</b> method can also be used to add a static playlist to the library.

Before calling this method, you must have full access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-remove">IWMPMediaCollection::remove</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-importplaylist">IWMPPlaylistCollection::importPlaylist</a>