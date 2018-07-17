---
UID: NN:certexit.ICertExit2
title: ICertExit2
author: windows-sdk-content
description: Provide communications between the Certificate Services server and an exit module.
old-location: security\icertexit2.htm
old-project: SecCrypto
ms.assetid: a9d66aeb-b596-4d50-9c07-b760cdf4f8c0
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICertExit2, ICertExit2 interface [Security], ICertExit2 interface [Security],described, _certsrv_icertexit2, certexit/ICertExit2, security.icertexit2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certexit.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certexit.h
api_name:
 - ICertExit2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertExit2</b> interface inherits from <a href="https://msdn.microsoft.com/731c4f3c-20b4-4f3d-8241-a94cdf656fe5">ICertExit</a> and <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>. <b>ICertExit2</b> also has these types of members:
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

