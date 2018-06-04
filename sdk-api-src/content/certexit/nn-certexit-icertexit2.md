---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ICertExit2 interface


## -description


The <b>ICertExit2</b> interface is one of two interfaces that   provide communications between  the Certificate Services server and an exit module.
<div class="alert"><b>Note</b>  The exit module can communicate with the Certificate Services server by using the <a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a> interface.</div><div> </div>The Certificate Services server calls the <b>ICertExit2</b> methods to perform the following tasks:<ul>
<li>Initialize the Certificate Services server.</li>
<li>Notify the exit module of an event such as certificate issuance, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CRL</a> issuance, or server shutdown, has occurred.</li>
<li>Retrieve a description of the exit module.</li>
<li>Retrieve the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface implemented by the exit module. The methods of this interface allows the Certificate Services server to configure the exit module as well as set and retrieve the exit module properties.</li>
</ul>


<b>ICertExit2</b> is defined in Certexit.h. When you create your program, however, use Certsrv.h as the include file.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertExit2</b> interface inherits from <a href="https://msdn.microsoft.com/731c4f3c-20b4-4f3d-8241-a94cdf656fe5">ICertExit</a> and <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>. <b>ICertExit2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertExit2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Returns a description of the exit module and its function.</p> (Inherited from <a href="https://msdn.microsoft.com/731c4f3c-20b4-4f3d-8241-a94cdf656fe5">ICertExit</a><b>ICertExit2</b><b>CCertExit2</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f0c1b63-fd09-43b9-9f88-fab154d94e94">GetManageModule</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface implemented by the exit module.</p> (Inherited from <b>ICertExit2</b><b>CCertExit2</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Called by the server engine when it initializes itself.</p> (Inherited from <a href="https://msdn.microsoft.com/731c4f3c-20b4-4f3d-8241-a94cdf656fe5">ICertExit</a><b>ICertExit2</b><b>CCertExit2</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebe4ef0c-5778-4a62-b112-9b16b250814f">Notify</a>
</td>
<td align="left" width="63%">
Called by the server engine to notify an exit module that an event has occurred.</p> (Inherited from <a href="https://msdn.microsoft.com/731c4f3c-20b4-4f3d-8241-a94cdf656fe5">ICertExit</a><b>ICertExit2</b><b>CCertExit2</b>)</td>
</tr>
</table> 

