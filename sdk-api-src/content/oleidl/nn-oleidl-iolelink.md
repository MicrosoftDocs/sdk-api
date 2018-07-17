---
UID: NN:oleidl.IOleLink
title: IOleLink
author: windows-sdk-content
description: Enables a linked object to provide its container with functions pertaining to linking.
old-location: com\iolelink.htm
old-project: com
ms.assetid: 4a34a90d-df1b-4bbf-8365-9d741c18ff74
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IOleLink, IOleLink interface [COM], IOleLink interface [COM],described, _ole_iolelink, com.iolelink, oleidl/IOleLink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleLink
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: ADAM
---

# IOleLink interface


## -description


Enables a linked object to provide its container with functions pertaining to linking. The most important of these functions is binding to the link source, that is, activating the connection to the document that stores the linked object's native data. <b>IOleLink</b> also defines functions for managing information about the linked object, such as the location of the link source and the cached presentation data for the linked object.

A container application can distinguish between embedded objects and linked objects by querying for <b>IOleLink</b>; only linked objects implement <b>IOleLink</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleLink</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleLink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleLink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/791fbb3c-6b73-490c-a69b-ba58fd386de4">BindIfRunning</a>
</td>
<td align="left" width="63%">
Activates the connection between the linked object and the link source if the link source is already running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fadd27d-cb2c-47fc-891a-16f82bdac0f6">BindToSource</a>
</td>
<td align="left" width="63%">
Activates the connection to the link source by binding the moniker stored within the linked object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37d24337-eacc-453a-9a90-043ec9b35e9c">GetBoundSource</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the link source if the connection is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4c5bc82-f423-4a02-b8d4-49b38a9c0f42">GetSourceDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the link source of the linked object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef447726-7aef-45c4-a522-a8de9a3e6b74">GetSourceMoniker</a>
</td>
<td align="left" width="63%">
Retrieves the moniker identifying the link source of a linked object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cb91b48-0026-4afa-80ab-16ac6fbce04d">GetUpdateOptions</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating how often the linked object updates its cached data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/762d021f-4bf1-4f90-bf41-065b8810de47">SetSourceDisplayName</a>
</td>
<td align="left" width="63%">
Sets the display name for the link source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85fe1d28-d9c6-46b4-abff-6afce9ff3cd0">SetSourceMoniker</a>
</td>
<td align="left" width="63%">
Sets the moniker for the link source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/310c25b5-a2f6-4ed7-8673-c53809fad32f">SetUpdateOptions</a>
</td>
<td align="left" width="63%">
Specifies how often a linked object should update its cached data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a678944-b4ba-47d8-9a89-470762efc6f9">UnbindSource</a>
</td>
<td align="left" width="63%">
Breaks the connection between a linked object and its link source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Updates the compound document's cached data for a linked object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>
 

 

