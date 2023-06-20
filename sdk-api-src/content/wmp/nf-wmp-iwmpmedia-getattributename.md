---
UID: NF:wmp.IWMPMedia.getAttributeName
title: IWMPMedia::getAttributeName (wmp.h)
description: The getAttributeName method retrieves the name of the attribute corresponding to the specified index.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","getAttributeName method","IWMPMedia.getAttributeName","IWMPMedia2 interface [Windows Media Player]","getAttributeName method","IWMPMedia2::getAttributeName","IWMPMedia3 interface [Windows Media Player]","getAttributeName method","IWMPMedia3::getAttributeName","IWMPMedia::getAttributeName","IWMPMediagetAttributeName","getAttributeName","getAttributeName method [Windows Media Player]","getAttributeName method [Windows Media Player]","IWMPMedia interface","getAttributeName method [Windows Media Player]","IWMPMedia2 interface","getAttributeName method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_getattributename","wmp/IWMPMedia2::getAttributeName","wmp/IWMPMedia3::getAttributeName","wmp/IWMPMedia::getAttributeName"]
old-location: wmp\iwmpmedia_getattributename.htm
tech.root: WMP
ms.assetid: cb04e464-44dd-41ba-9296-f13aca9ef54e
ms.date: 4/26/2023
ms.keywords: IWMPMedia interface [Windows Media Player],getAttributeName method, IWMPMedia.getAttributeName, IWMPMedia2 interface [Windows Media Player],getAttributeName method, IWMPMedia2::getAttributeName, IWMPMedia3 interface [Windows Media Player],getAttributeName method, IWMPMedia3::getAttributeName, IWMPMedia::getAttributeName, IWMPMediagetAttributeName, getAttributeName, getAttributeName method [Windows Media Player], getAttributeName method [Windows Media Player],IWMPMedia interface, getAttributeName method [Windows Media Player],IWMPMedia2 interface, getAttributeName method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_getattributename, wmp/IWMPMedia2::getAttributeName, wmp/IWMPMedia3::getAttributeName, wmp/IWMPMedia::getAttributeName
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
 - IWMPMedia::getAttributeName
 - wmp/IWMPMedia::getAttributeName
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
 - IWMPMedia.getAttributeName
 - IWMPMedia2.getAttributeName
 - IWMPMedia3.getAttributeName
---

# IWMPMedia::getAttributeName


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getAttributeName</b> method retrieves the name of the attribute corresponding to the specified index.

## -parameters

### -param lIndex [in]

<b>long</b> containing the index.

### -param pbstrItemName [out]

Pointer to a <b>BSTR</b> containing the attribute name.

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

The attribute name returned can be used in conjunction with <b>getItemInfo</b> to retrieve the value for a specific named attribute.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="/windows/desktop/WMP/attribute-reference">Attribute Reference</a>.

<b>Windows Media Player 10 Mobile:</b> Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo">IWMPMedia::getItemInfo</a>