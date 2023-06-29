---
UID: NF:wmp.IWMPMedia3.getItemInfoByType
title: IWMPMedia3::getItemInfoByType (wmp.h)
description: The getItemInfoByType method retrieves the value of the attribute corresponding to the specified attribute type and index.
helpviewer_keywords: ["IWMPMedia3 interface [Windows Media Player]","getItemInfoByType method","IWMPMedia3.getItemInfoByType","IWMPMedia3::getItemInfoByType","IWMPMedia3getItemInfoByType","getItemInfoByType","getItemInfoByType method [Windows Media Player]","getItemInfoByType method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia3_getiteminfobytype","wmp/IWMPMedia3::getItemInfoByType"]
old-location: wmp\iwmpmedia3_getiteminfobytype.htm
tech.root: WMP
ms.assetid: 2a77029b-fbae-49af-bd91-c688c11b3b16
ms.date: 4/26/2023
ms.keywords: IWMPMedia3 interface [Windows Media Player],getItemInfoByType method, IWMPMedia3.getItemInfoByType, IWMPMedia3::getItemInfoByType, IWMPMedia3getItemInfoByType, getItemInfoByType, getItemInfoByType method [Windows Media Player], getItemInfoByType method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia3_getiteminfobytype, wmp/IWMPMedia3::getItemInfoByType
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
 - IWMPMedia3::getItemInfoByType
 - wmp/IWMPMedia3::getItemInfoByType
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
 - IWMPMedia3.getItemInfoByType
---

# IWMPMedia3::getItemInfoByType


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getItemInfoByType</b> method retrieves the value of the attribute corresponding to the specified attribute type and index.

## -parameters

### -param bstrType [in]

<b>BSTR</b> containing the type.

### -param bstrLanguage [in]

<b>BSTR</b> containing the language. If the value is set to null or "" (empty string), the current locale string is used. Otherwise, the value must be a valid RFC 1766 language string such as "en-us".

### -param lIndex [in]

<b>long</b> containing the index.

### -param pvarValue [out]

Pointer to a <b>VARIANT</b> that contains the returned value.

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

This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.

This method supports attributes with multiple values and attributes with complex values. The <b>getItemInfo</b> method does not support attributes with multiple values and attributes with complex values.

The <b>attributeCount</b> method retrieves the number of attribute names available for a given media item. Index numbers can then be used with the <b>getAttributeName</b> method to determine the name of each available attribute. Individual attribute names can be passed to the <i>name</i> parameter of <b>getItemInfoByType</b>.

The <b>getAttributeCountByType</b> method returns the number of attributes that correspond to a particular attribute name for a given media item. Index numbers can then be passed to the <i>index</i> parameter of <b>getItemInfoByType</b>. This is useful when a media item has been categorized under multiple genres, for example.

The set of attributes available from sources other than the local library (remote libraries, portable devices, or CDs is defined by the other sources.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia3">IWMPMedia3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getattributecountbytype">IWMPMedia3::getAttributeCountByType</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getattributename">IWMPMedia::getAttributeName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo">IWMPMedia::getItemInfo</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_attributecount">IWMPMedia::get_attributeCount</a>