---
UID: NF:wmp.IWMPMediaCollection.getAll
title: IWMPMediaCollection::getAll (wmp.h)
description: The getAll method retrieves a pointer to an IWMPPlaylist interface. This interface corresponds to the playlist that contains all media items in the library.
helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","getAll method","IWMPMediaCollection.getAll","IWMPMediaCollection::getAll","IWMPMediaCollectiongetAll","getAll","getAll method [Windows Media Player]","getAll method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_getall","wmp/IWMPMediaCollection::getAll"]
old-location: wmp\iwmpmediacollection_getall.htm
tech.root: WMP
ms.assetid: db06194c-36e2-4494-b464-c08f6983bdc1
ms.date: 4/26/2023
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getAll method, IWMPMediaCollection.getAll, IWMPMediaCollection::getAll, IWMPMediaCollectiongetAll, getAll, getAll method [Windows Media Player], getAll method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getall, wmp/IWMPMediaCollection::getAll
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
 - IWMPMediaCollection::getAll
 - wmp/IWMPMediaCollection::getAll
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
 - IWMPMediaCollection.getAll
---

# IWMPMediaCollection::getAll


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getAll</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface corresponds to the playlist that contains all media items in the library.

## -parameters

### -param ppMediaItems [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface for the playlist that contains all of the requested media items.

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

There are two ways you ways you can retrieve an <b>IWMPMediaCollection</b> interface, and the behavior of the <b>getAll</b> method depends on which of those two ways you use. If you retrieve the interface by calling <a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection">IWMPCore::get_mediaCollection</a>, then the <b>getAll</b> method returns all the media items in the library.If you retrieve the interface by calling <a href="/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection">IWMPLibrary::get_mediaCollection</a>, then the <b>getAll</b> method returns only the audio items in the library.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>