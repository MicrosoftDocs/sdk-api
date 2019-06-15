---
UID: NN:faxcomex.IFaxActivity
title: IFaxActivity (faxcomex.h)
author: windows-sdk-content
description: The IFaxActivity interface defines a read-only configuration object.
old-location: fax\_mfax_faxactivity_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4k55_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxActivity, IFaxActivity interface [Fax Service], IFaxActivity interface [Fax Service],described, _mfax_faxactivity_cpp, fax._mfax_faxactivity_cpp, faxcomex/IFaxActivity
ms.topic: interface
f1_keywords: ["faxcomex/IFaxActivity"]
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxActivity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxActivity interface


## -description


The <b>IFaxActivity</b> interface defines a read-only configuration object. The object permits a fax client application to access information about the activity on a connected fax server. For example, you can retrieve information about the number of outbound routing jobs that are currently executing, those that are pending processing, and those that are waiting in the job queue.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxActivity</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxActivity</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-refresh-vb">IFaxActivity::Refresh</a> method refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity">FaxActivity</a> information from the fax server.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-refresh-vb">IFaxActivity::Refresh</a> method refreshes <b>IFaxActivity</b> information from the fax server.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-incomingmessages-vb">IncomingMessages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-incomingmessages-vb">IFaxActivity::get_IncomingMessages</a> property is a number that represents the total number of incoming fax jobs that the fax service is currently in the process of receiving.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-outgoingmessages-vb">OutgoingMessages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-outgoingmessages-vb">IFaxActivity::get_OutgoingMessages</a> property is a number that represents the total number of outgoing fax jobs that the fax service is in the process of sending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-queuedmessages-vb">QueuedMessages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-queuedmessages-vb">IFaxActivity::get_QueuedMessages</a> property is a number that represents the total number of fax jobs in the fax job queue that are pending processing. This does not include jobs for which the number of retries has been exceeded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-routingmessages-vb">RoutingMessages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity-routingmessages-vb">IFaxActivity::get_RoutingMessages</a> property is a number that represents the total number of incoming fax jobs that the fax service is currently routing.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxActivity</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivity">FaxActivity</a> object.

You can configure whether the fax service logs information about incoming and outgoing fax jobs in an activity log database. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> configuration object permits configuration of the activity logging options that the fax service uses.



