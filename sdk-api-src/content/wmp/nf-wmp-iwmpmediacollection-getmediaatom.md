---
UID: NF:wmp.IWMPMediaCollection.getMediaAtom
title: IWMPMediaCollection::getMediaAtom (wmp.h)
description: The getMediaAtom method retrieves the index at which a given attribute resides within the set of available attributes.
helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","getMediaAtom method","IWMPMediaCollection.getMediaAtom","IWMPMediaCollection::getMediaAtom","IWMPMediaCollectiongetMediaAtom","getMediaAtom","getMediaAtom method [Windows Media Player]","getMediaAtom method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_getmediaatom","wmp/IWMPMediaCollection::getMediaAtom"]
old-location: wmp\iwmpmediacollection_getmediaatom.htm
tech.root: WMP
ms.assetid: 22024108-398e-4a05-b5ed-311583c69497
ms.date: 4/26/2023
ms.keywords: IWMPMediaCollection interface [Windows Media Player],getMediaAtom method, IWMPMediaCollection.getMediaAtom, IWMPMediaCollection::getMediaAtom, IWMPMediaCollectiongetMediaAtom, getMediaAtom, getMediaAtom method [Windows Media Player], getMediaAtom method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_getmediaatom, wmp/IWMPMediaCollection::getMediaAtom
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
 - IWMPMediaCollection::getMediaAtom
 - wmp/IWMPMediaCollection::getMediaAtom
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
 - IWMPMediaCollection.getMediaAtom
---

# IWMPMediaCollection::getMediaAtom


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getMediaAtom</b> method retrieves the index at which a given attribute resides within the set of available attributes.

## -parameters

### -param bstrItemName [in]

String containing the name of the item for which the index should be retrieved.

### -param plAtom [out]

Pointer to a <b>long</b> containing the index.

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

The index number retrieved with this method can be passed to the <b>IWMPMedia::getItemInfoByAtom</b> to access attribute values. This technique is generally more efficient when working with large playlists than accessing an attribute value by name through <b>IWMPMedia::getItemInfo</b>.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo">IWMPMedia::getItemInfo</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfobyatom">IWMPMedia::getItemInfoByAtom</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>