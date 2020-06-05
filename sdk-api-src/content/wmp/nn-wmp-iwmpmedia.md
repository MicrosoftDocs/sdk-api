---
UID: NN:wmp.IWMPMedia
title: IWMPMedia (wmp.h)
description: Use the IWMPMedia interface to set and retrieve the properties of a media item.helpviewer_keywords: ["IWMPMedia","IWMPMedia interface [Windows Media Player]","IWMPMedia interface [Windows Media Player]","described","IWMPMediaInterface","wmp.iwmpmedia","wmp/IWMPMedia"]
old-location: wmp\iwmpmedia.htm
tech.root: WMP
ms.assetid: 2311067c-b731-47d2-880d-73870fee7694
ms.date: 12/05/2018
ms.keywords: IWMPMedia, IWMPMedia interface [Windows Media Player], IWMPMedia interface [Windows Media Player],described, IWMPMediaInterface, wmp.iwmpmedia, wmp/IWMPMedia
f1_keywords:
- wmp/IWMPMedia
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.h
api_name:
- IWMPMedia
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMedia interface


## -description



Use the <b>IWMPMedia</b> interface to set and retrieve the properties of a media item.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMedia</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPMedia</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPMedia</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_attributecount">get_attributeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes that can be queried and/or set for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_duration">get_duration</a>
</td>
<td align="left" width="63%">
Retrieves the duration in seconds of the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_durationstring">get_durationString</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the duration of the current media item in HH:MM:SS format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_imagesourceheight">get_imageSourceHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the current media item in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_imagesourcewidth">get_imageSourceWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the current media item in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical">get_isIdentical</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified object is the same as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_markercount">get_markerCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of markers in the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_name">get_name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl">get_sourceURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getattributename">getAttributeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the attribute corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified attribute for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfobyatom">getItemInfoByAtom</a>
</td>
<td align="left" width="63%">
Retrieves the value of the attribute with the specified index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getmarkername">getMarkerName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the marker at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getmarkertime">getMarkerTime</a>
</td>
<td align="left" width="63%">
Retrieves the time of the marker at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-ismemberof">isMemberOf</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified media item is a member of the specified playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-isreadonlyitem">isReadOnlyItem</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the attributes of the specified media item can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-put_name">put_name</a>
</td>
<td align="left" width="63%">
Sets the name of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-setiteminfo">setItemInfo</a>
</td>
<td align="left" width="63%">
Sets the value of the specified attribute for the media item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

