---
UID: NN:wmp.IWMPMedia
title: IWMPMedia
author: windows-sdk-content
description: Use the IWMPMedia interface to set and retrieve the properties of a media item.
old-location: wmp\iwmpmedia.htm
old-project: WMP
ms.assetid: 2311067c-b731-47d2-880d-73870fee7694
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPMedia, IWMPMedia interface [Windows Media Player], IWMPMedia interface [Windows Media Player],described, IWMPMediaInterface, wmp.iwmpmedia, wmp/IWMPMedia
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMedia interface


## -description



Use the <b>IWMPMedia</b> interface to set and retrieve the properties of a media item.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPMedia</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPMedia</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/33e29da2-7439-41d1-9dd9-9b66e87aeb4b">get_attributeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of attributes that can be queried and/or set for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40313888-faa0-499e-9133-dc437f5ad44f">get_duration</a>
</td>
<td align="left" width="63%">
Retrieves the duration in seconds of the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/540f4780-850f-41ec-940c-e8f7d3c96e6b">get_durationString</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the duration of the current media item in HH:MM:SS format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f39049ad-3641-4885-a8e4-f1e46b181f6e">get_imageSourceHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height of the current media item in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57480abb-9852-46a5-a6e4-2a1ba517a9cb">get_imageSourceWidth</a>
</td>
<td align="left" width="63%">
Retrieves the width of the current media item in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ec54350-0359-4759-a6ba-6132ce33feff">get_isIdentical</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified object is the same as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e97c8d26-fa6a-4791-a698-b742eaf980eb">get_markerCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of markers in the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83bb3495-a12d-48a8-864c-3cd636866308">get_name</a>
</td>
<td align="left" width="63%">
Retrieves the name of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99a9bd0f-0429-41b0-96fc-b84d895f6b38">get_sourceURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb04e464-44dd-41ba-9296-f13aca9ef54e">getAttributeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the attribute corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee964f68-d44c-4e66-908b-09070a96d96f">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified attribute for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2e803df-84f2-4c23-9872-a5435977d189">getItemInfoByAtom</a>
</td>
<td align="left" width="63%">
Retrieves the value of the attribute with the specified index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86c3931f-5790-43f5-896d-1728c38247a9">getMarkerName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the marker at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6c2484d-8167-4305-9467-f9b2b7fedc32">getMarkerTime</a>
</td>
<td align="left" width="63%">
Retrieves the time of the marker at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ca46263-1e8e-42db-a131-e7534f79ca8e">isMemberOf</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the specified media item is a member of the specified playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8b2dd45-3e3f-4325-b4d0-939abbc425e1">isReadOnlyItem</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the attributes of the specified media item can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cf6cff8-c5d1-4d10-8d32-764e35ef7ba2">put_name</a>
</td>
<td align="left" width="63%">
Sets the name of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/919fe92f-9519-4229-8097-4970a8f6cc25">setItemInfo</a>
</td>
<td align="left" width="63%">
Sets the value of the specified attribute for the media item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

