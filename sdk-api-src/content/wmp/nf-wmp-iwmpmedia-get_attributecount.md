---
UID: NF:wmp.IWMPMedia.get_attributeCount
title: IWMPMedia::get_attributeCount (wmp.h)
description: The get_attributeCount method retrieves the number of attributes that can be queried and/or set for the media item.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","get_attributeCount method","IWMPMedia.get_attributeCount","IWMPMedia2 interface [Windows Media Player]","get_attributeCount method","IWMPMedia2::get_attributeCount","IWMPMedia3 interface [Windows Media Player]","get_attributeCount method","IWMPMedia3::get_attributeCount","IWMPMedia::get_attributeCount","IWMPMediaget_attributeCount","get_attributeCount","get_attributeCount method [Windows Media Player]","get_attributeCount method [Windows Media Player]","IWMPMedia interface","get_attributeCount method [Windows Media Player]","IWMPMedia2 interface","get_attributeCount method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_get_attributecount","wmp/IWMPMedia2::get_attributeCount","wmp/IWMPMedia3::get_attributeCount","wmp/IWMPMedia::get_attributeCount"]
old-location: wmp\iwmpmedia_get_attributecount.htm
tech.root: WMP
ms.assetid: 33e29da2-7439-41d1-9dd9-9b66e87aeb4b
ms.date: 4/26/2023
ms.keywords: IWMPMedia interface [Windows Media Player],get_attributeCount method, IWMPMedia.get_attributeCount, IWMPMedia2 interface [Windows Media Player],get_attributeCount method, IWMPMedia2::get_attributeCount, IWMPMedia3 interface [Windows Media Player],get_attributeCount method, IWMPMedia3::get_attributeCount, IWMPMedia::get_attributeCount, IWMPMediaget_attributeCount, get_attributeCount, get_attributeCount method [Windows Media Player], get_attributeCount method [Windows Media Player],IWMPMedia interface, get_attributeCount method [Windows Media Player],IWMPMedia2 interface, get_attributeCount method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_attributecount, wmp/IWMPMedia2::get_attributeCount, wmp/IWMPMedia3::get_attributeCount, wmp/IWMPMedia::get_attributeCount
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
 - IWMPMedia::get_attributeCount
 - wmp/IWMPMedia::get_attributeCount
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
 - IWMPMedia.get_attributeCount
 - IWMPMedia2.get_attributeCount
 - IWMPMedia3.get_attributeCount
---

# IWMPMedia::get_attributeCount


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_attributeCount</b> method retrieves the number of attributes that can be queried and/or set for the media item.

## -parameters

### -param plCount [out]

Pointer to a <b>long</b> containing the count.

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

For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="/windows/desktop/WMP/attribute-reference">Attribute Reference</a>.

<b>Windows Media Player 10 Mobile:</b> Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>