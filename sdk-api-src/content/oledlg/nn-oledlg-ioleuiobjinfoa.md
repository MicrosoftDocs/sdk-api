---
UID: NN:oledlg.IOleUIObjInfoA
title: IOleUIObjInfoA
author: windows-sdk-content
description: Implemented by containers and used by the container's Object Properties dialog box and by the Convert dialog box.
old-location: com\ioleuiobjinfo.htm
old-project: com
ms.assetid: 508dccb3-e98b-4f62-8bc3-98ca2b0d1349
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOleUIObjInfo, IOleUIObjInfo interface [COM], IOleUIObjInfo interface [COM],described, IOleUIObjInfoA, IOleUIObjInfoW, _ole_IOleUIObjInfo, com.ioleuiobjinfo, oledlg/IOleUIObjInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oledlg.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: OLEUIPASTEFLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleDlg.h
api_name:
 - IOleUIObjInfo
 - IOleUIObjInfoW
 - IOleUIObjInfoA
product: Windows
targetos: Windows
req.lib: OleDlg.lib
req.dll: OleDlg.dll
req.irql: 
req.product: ADAM
---

# IOleUIObjInfoA interface


## -description


Implemented by containers and used by the container's <b>Object Properties</b> dialog box and by the <b>Convert</b> dialog box. It provides information used by the <b>General</b> and <b>View</b> pages of the <b>Object Properties</b> dialog box , which display information about the object's size, location, type, and name. It also allows the object to be converted using the <b>Convert</b> dialog box. The <b>View</b> page allows the object's icon to be modified from its original form, and its display aspect to be changed (iconic versus content). Optionally, you can have your implementation of this interface allow the scale of the object to be changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleUIObjInfo</b> interface inherits from <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>. <b>IOleUIObjInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleUIObjInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44611ed3-35de-4b20-adae-d3a28aa11944">ConvertObject</a>
</td>
<td align="left" width="63%">
Converts the object to the type of the specified CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45416493-7f0b-4bef-b785-513d4f404541">GetConvertInfo</a>
</td>
<td align="left" width="63%">
Gets the conversion information associated with the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d09aafd0-0f4b-42c4-b1e6-0656cf0bd02d">GetObjectInfo</a>
</td>
<td align="left" width="63%">
Gets the size, type, name, and location information about an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e9774b6-1264-48d4-b5fb-c43b67e29f6e">GetViewInfo</a>
</td>
<td align="left" width="63%">
Gets the view information associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83d88f33-448f-4b8f-9c82-b6aaa4e8ff4a">SetViewInfo</a>
</td>
<td align="left" width="63%">
Sets the view information associated with the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a>
 

 

