---
UID: NN:oledlg.IOleUILinkContainerW
title: IOleUILinkContainerW
author: windows-sdk-content
description: Implemented by containers and used by OLE common dialog boxes. It supports these dialog boxes by providing the methods needed to manage a container's links.
old-location: com\ioleuilinkcontainer.htm
tech.root: com
ms.assetid: 7fc0aab3-7476-49ec-8a1d-3f4851f9f31c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IOleUILinkContainer, IOleUILinkContainer interface [COM], IOleUILinkContainer interface [COM],described, IOleUILinkContainerA, IOleUILinkContainerW, _ole_IOleUILinkContainer, com.ioleuilinkcontainer, oledlg/IOleUILinkContainer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oledlg.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleDlg.h
api_name:
 - IOleUILinkContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleUILinkContainerW interface


## -description


Implemented by containers and used by OLE common dialog boxes. It supports these dialog boxes by providing the methods needed to manage a container's links.

The <b>IOleUILinkContainer</b> methods enumerate the links associated with a container, and specify how they should be updated, automatically or manually. They change the source of a link and obtain information associated with a link. They also open a link's source document, update links, and break a link to the source.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleUILinkContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOleUILinkContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleUILinkContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97099e4d-20ea-47fb-8ca8-27330f980038">CancelLink</a>
</td>
<td align="left" width="63%">
Disconnects the selected links.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10f1bc84-cc09-4a41-8f55-21314338f636">GetLinkSource</a>
</td>
<td align="left" width="63%">
Retrieves information about a link that can be displayed in the <b>Links</b> dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/136894a6-ddf6-4a47-80f5-997625362536">GetLinkUpdateOptions</a>
</td>
<td align="left" width="63%">
Determines the current update options for the link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60246b31-3677-4424-a131-840feeca030f">GetNextLink</a>
</td>
<td align="left" width="63%">
Enumerates the links in a container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc732a2f-f13d-4d08-a81d-292dd2ba1140">OpenLinkSource</a>
</td>
<td align="left" width="63%">
Opens the link's source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c76723e8-e895-4ba1-9ba1-7e56a44cc5f2">SetLinkSource</a>
</td>
<td align="left" width="63%">
Changes the source of a link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2a7758d-9692-4e3c-8186-b74530299a6a">SetLinkUpdateOptions</a>
</td>
<td align="left" width="63%">
Sets a link's update options to automatic or manual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fccee32a-3a6f-4ef8-9ca7-c5b664ee03cf">UpdateLink</a>
</td>
<td align="left" width="63%">
Forces a link to connect to its source and update.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0a139936-bda4-40c8-85d6-b52ff042f2d9">OLEUIEDITLINKS</a>



<a href="https://msdn.microsoft.com/53ff17aa-3135-462e-885d-3bfbb74ed1c5">OleUIChangeSource</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>



<a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a>



<a href="https://msdn.microsoft.com/f280b061-45d8-484d-9fe1-ec4d85288bc6">OleUIUpdateLinks</a>
 

 

