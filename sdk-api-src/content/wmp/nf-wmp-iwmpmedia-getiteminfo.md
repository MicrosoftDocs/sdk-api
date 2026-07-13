---
UID: NF:wmp.IWMPMedia.getItemInfo
title: IWMPMedia::getItemInfo (wmp.h)
description: The getItemInfo method retrieves the value of the specified attribute for the media item.
helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","getItemInfo method","IWMPMedia.getItemInfo","IWMPMedia2 interface [Windows Media Player]","getItemInfo method","IWMPMedia2::getItemInfo","IWMPMedia3 interface [Windows Media Player]","getItemInfo method","IWMPMedia3::getItemInfo","IWMPMedia::getItemInfo","IWMPMediagetItemInfo","getItemInfo","getItemInfo method [Windows Media Player]","getItemInfo method [Windows Media Player]","IWMPMedia interface","getItemInfo method [Windows Media Player]","IWMPMedia2 interface","getItemInfo method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_getiteminfo","wmp/IWMPMedia2::getItemInfo","wmp/IWMPMedia3::getItemInfo","wmp/IWMPMedia::getItemInfo"]
old-location: wmp\iwmpmedia_getiteminfo.htm
tech.root: WMP
ms.assetid: ee964f68-d44c-4e66-908b-09070a96d96f
ms.date: 4/26/2023
ms.keywords: IWMPMedia interface [Windows Media Player],getItemInfo method, IWMPMedia.getItemInfo, IWMPMedia2 interface [Windows Media Player],getItemInfo method, IWMPMedia2::getItemInfo, IWMPMedia3 interface [Windows Media Player],getItemInfo method, IWMPMedia3::getItemInfo, IWMPMedia::getItemInfo, IWMPMediagetItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPMedia interface, getItemInfo method [Windows Media Player],IWMPMedia2 interface, getItemInfo method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_getiteminfo, wmp/IWMPMedia2::getItemInfo, wmp/IWMPMedia3::getItemInfo, wmp/IWMPMedia::getItemInfo
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
 - IWMPMedia::getItemInfo
 - wmp/IWMPMedia::getItemInfo
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
 - IWMPMedia.getItemInfo
 - IWMPMedia2.getItemInfo
 - IWMPMedia3.getItemInfo
---

# IWMPMedia::getItemInfo


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getItemInfo</b> method retrieves the value of the specified attribute for the media item.

## -parameters

### -param bstrItemName [in]

<b>BSTR</b> containing the item name.

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

This method retrieves the metadata for an individual media item or a media item that is part of a playlist.

The <b>get_attributeCount</b> method retrieves the number of attribute names available for a given media item. Index numbers can then be used with the <b>getAttributeName</b> method to determine the name of each available attribute. Individual attribute names can be passed to <b>getItemInfo</b>.

To retrieve attributes with multiple values and attributes with complex values, use the <b>getItemInfoByType</b> method.

The set of attributes available from sources other than the local library (remote libraries, portable devices, or CDs) is defined by the other sources.

Before calling this method, you must have Read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that 

is exposed over UPnP. Other devices can then navigate and browse the libraries. 


In Windows 7, an application can use the Windows Media Player <a href="/windows/desktop/WMP/trackingid-attribute">TrackingID</a> and <a href="/windows/desktop/WMP/mediatype-attribute">MediaType</a> attributes to construct the object ID of each item in the CDS. Note that this construction might change in future versions of Windows. The application passes each of these attribute strings in the <i>bstrItemName</i> parameter in a call to <b>getItemInfo</b>. <b>getItemInfo</b> returns the value for each attribute in a variable to which the   <i>pbstrVal</i> parameter points.  The application then uses the following syntax to construct each object ID:

<i>TrackingID</i>.0.<i>MediaTypeID</i>

This syntax has the  following meaning:

<ul>
<li><i>TrackingID</i> is the string that is stored in the Windows Media Player <a href="/windows/desktop/WMP/trackingid-attribute">TrackingID</a> attribute of the media item.</li>
<li><i>MediaTypeID</i> depends on the value of the <a href="/windows/desktop/WMP/mediatype-attribute">MediaType</a> 

attribute, as shown in the following table:<table>
<tr>
<th>MediaType attribute</th>
<th>MediaTypeID</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/WMP/audio-item-attributes">Audio Items</a>
</td>
<td>4</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/WMP/photo-item-attributes">Photo Items</a>
</td>
<td>B</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/WMP/video-item-attributes">Video Items</a>
</td>
<td>8</td>
</tr>
</table>
 

</li>
</ul>
<b>Windows Media Player 10 Mobile:</b> Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.

## -see-also

<a href="/windows/desktop/WMP/attribute-reference">Attribute Reference</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype">IWMPMedia3::getItemInfoByType</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getattributename">IWMPMedia::getAttributeName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_attributecount">IWMPMedia::get_attributeCount</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmedia-setiteminfo">IWMPMedia::setItemInfo</a>