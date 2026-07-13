---
UID: NF:wmp.IWMPMedia.getItemInfoByAtom
title: IWMPMedia::getItemInfoByAtom (wmp.h)
description: The getItemInfoByAtom method retrieves the value of the attribute with the specified index number.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","getItemInfoByAtom method","IWMPMedia.getItemInfoByAtom","IWMPMedia2 interface [Windows Media Player]","getItemInfoByAtom method","IWMPMedia2::getItemInfoByAtom","IWMPMedia3 interface [Windows Media Player]","getItemInfoByAtom method","IWMPMedia3::getItemInfoByAtom","IWMPMedia::getItemInfoByAtom","IWMPMediagetItemInfoByAtom","getItemInfoByAtom","getItemInfoByAtom method [Windows Media Player]","getItemInfoByAtom method [Windows Media Player]","IWMPMedia interface","getItemInfoByAtom method [Windows Media Player]","IWMPMedia2 interface","getItemInfoByAtom method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_getiteminfobyatom","wmp/IWMPMedia2::getItemInfoByAtom","wmp/IWMPMedia3::getItemInfoByAtom","wmp/IWMPMedia::getItemInfoByAtom"]
old-location: wmp\iwmpmedia_getiteminfobyatom.htm
tech.root: WMP
ms.assetid: c2e803df-84f2-4c23-9872-a5435977d189
ms.date: 4/26/2023
ms.keywords: IWMPMedia interface [Windows Media Player],getItemInfoByAtom method, IWMPMedia.getItemInfoByAtom, IWMPMedia2 interface [Windows Media Player],getItemInfoByAtom method, IWMPMedia2::getItemInfoByAtom, IWMPMedia3 interface [Windows Media Player],getItemInfoByAtom method, IWMPMedia3::getItemInfoByAtom, IWMPMedia::getItemInfoByAtom, IWMPMediagetItemInfoByAtom, getItemInfoByAtom, getItemInfoByAtom method [Windows Media Player], getItemInfoByAtom method [Windows Media Player],IWMPMedia interface, getItemInfoByAtom method [Windows Media Player],IWMPMedia2 interface, getItemInfoByAtom method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_getiteminfobyatom, wmp/IWMPMedia2::getItemInfoByAtom, wmp/IWMPMedia3::getItemInfoByAtom, wmp/IWMPMedia::getItemInfoByAtom
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
 - IWMPMedia::getItemInfoByAtom
 - wmp/IWMPMedia::getItemInfoByAtom
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
 - IWMPMedia.getItemInfoByAtom
 - IWMPMedia2.getItemInfoByAtom
 - IWMPMedia3.getItemInfoByAtom
---

# IWMPMedia::getItemInfoByAtom


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getItemInfoByAtom</b> method retrieves the value of the attribute with the specified index number.

## -parameters

### -param lAtom [in]

<b>long</b> specifying the index at which a given attribute resides within the set of available attributes.

### -param pbstrVal [out]

Pointer to a <b>BSTR</b> containing the returned value.

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

This method can be used to retrieve metadata for a specific media item by using an attribute index number. The <b>get_attributeCount</b> method can be used to determine the number of attributes available for the media item.

The <b>getMediaAtom</b> method of the <b>MediaCollection</b> object can also be used to retrieve the index of a particular attribute. This technique is generally more efficient than the <b>getItemInfo</b> or <b>getItemInfoByType</b> methods when working with large playlists.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype">IWMPMedia3::getItemInfoByType</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo">IWMPMedia::getItemInfo</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_attributecount">IWMPMedia::get_attributeCount</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-setiteminfo">IWMPMedia::setItemInfo</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getmediaatom">IWMPMediaCollection::getMediaAtom</a>