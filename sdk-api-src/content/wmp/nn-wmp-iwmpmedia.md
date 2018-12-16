---
UID: NN:wmp.IWMPMedia
title: IWMPMedia
author: windows-sdk-content
description: Use the IWMPMedia interface to set and retrieve the properties of a media item.
old-location: wmp\iwmpmedia.htm
tech.root: WMP
ms.assetid: 2311067c-b731-47d2-880d-73870fee7694
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPMedia, IWMPMedia interface [Windows Media Player], IWMPMedia interface [Windows Media Player],described, IWMPMediaInterface, wmp.iwmpmedia, wmp/IWMPMedia
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMedia interface


## -description



Use the <b>IWMPMedia</b> interface to set and retrieve the properties of a media item.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMedia</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPMedia</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563435(v=VS.85).aspx">get_attributeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes that can be queried and/or set for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563436(v=VS.85).aspx">get_duration</a>
</td>
<td align="left" width="63%">
Retrieves the duration in seconds of the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563437(v=VS.85).aspx">get_durationString</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the duration of the current media item in HH:MM:SS format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563438(v=VS.85).aspx">get_imageSourceHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the current media item in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563439(v=VS.85).aspx">get_imageSourceWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the current media item in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563440(v=VS.85).aspx">get_isIdentical</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified object is the same as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563441(v=VS.85).aspx">get_markerCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of markers in the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563442(v=VS.85).aspx">get_name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563443(v=VS.85).aspx">get_sourceURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563430(v=VS.85).aspx">getAttributeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the attribute corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563431(v=VS.85).aspx">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified attribute for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563432(v=VS.85).aspx">getItemInfoByAtom</a>
</td>
<td align="left" width="63%">
Retrieves the value of the attribute with the specified index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563433(v=VS.85).aspx">getMarkerName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the marker at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563434(v=VS.85).aspx">getMarkerTime</a>
</td>
<td align="left" width="63%">
Retrieves the time of the marker at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563446(v=VS.85).aspx">isMemberOf</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified media item is a member of the specified playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563447(v=VS.85).aspx">isReadOnlyItem</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the attributes of the specified media item can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563448(v=VS.85).aspx">put_name</a>
</td>
<td align="left" width="63%">
Sets the name of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563449(v=VS.85).aspx">setItemInfo</a>
</td>
<td align="left" width="63%">
Sets the value of the specified attribute for the media item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

