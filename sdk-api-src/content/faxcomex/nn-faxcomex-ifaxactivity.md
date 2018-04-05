---
UID: NN:faxcomex.IFaxActivity
title: IFaxActivity
author: windows-driver-content
description: The IFaxActivity interface defines a read-only configuration object.
old-location: fax\_mfax_faxactivity_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4k55_cpp.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: IFaxActivity, IFaxActivity interface [Fax Service], IFaxActivity interface [Fax Service], described, _mfax_faxactivity_cpp, fax._mfax_faxactivity_cpp, faxcomex/IFaxActivity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxActivity
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxActivity interface


## -description


The <b>IFaxActivity</b> interface defines a read-only configuration object. The object permits a fax client application to access information about the activity on a connected fax server. For example, you can retrieve information about the number of outbound routing jobs that are currently executing, those that are pending processing, and those that are waiting in the job queue.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxActivity</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxActivity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxActivity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ca97780-0138-401e-a7e8-4af8ee3f8f43">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8ca97780-0138-401e-a7e8-4af8ee3f8f43">IFaxActivity::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/5d3a10cb-64ef-4b20-a882-7f5e2738a8a0">FaxActivity</a> information from the fax server.

The <a href="https://msdn.microsoft.com/8ca97780-0138-401e-a7e8-4af8ee3f8f43">IFaxActivity::Refresh</a> method refreshes <b>IFaxActivity</b> information from the fax server.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxActivity</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c66d7f36-86e4-42d7-baf6-e97b13aec760">IncomingMessages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c66d7f36-86e4-42d7-baf6-e97b13aec760">IFaxActivity::get_IncomingMessages</a> property is a number that represents the total number of incoming fax jobs that the fax service is currently in the process of receiving.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c7ee1601-195e-4bc3-b071-6ce94194c84a">OutgoingMessages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c7ee1601-195e-4bc3-b071-6ce94194c84a">IFaxActivity::get_OutgoingMessages</a> property is a number that represents the total number of outgoing fax jobs that the fax service is in the process of sending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/eb578164-afcc-4946-891a-69878b6d9b6d">QueuedMessages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/eb578164-afcc-4946-891a-69878b6d9b6d">IFaxActivity::get_QueuedMessages</a> property is a number that represents the total number of fax jobs in the fax job queue that are pending processing. This does not include jobs for which the number of retries has been exceeded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6c650643-462c-484c-8ef8-ad217e7a463b">RoutingMessages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6c650643-462c-484c-8ef8-ad217e7a463b">IFaxActivity::get_RoutingMessages</a> property is a number that represents the total number of incoming fax jobs that the fax service is currently routing.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxActivity</b> is provided as the <a href="https://msdn.microsoft.com/5d3a10cb-64ef-4b20-a882-7f5e2738a8a0">FaxActivity</a> object.

You can configure whether the fax service logs information about incoming and outgoing fax jobs in an activity log database. The <a href="https://msdn.microsoft.com/225afdb8-7249-4aa5-bbde-638adf02eb41">FaxActivityLogging</a> configuration object permits configuration of the activity logging options that the fax service uses.



