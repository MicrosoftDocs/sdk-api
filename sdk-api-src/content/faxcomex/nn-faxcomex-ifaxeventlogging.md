---
UID: NN:faxcomex.IFaxEventLogging
title: IFaxEventLogging (faxcomex.h)
author: windows-sdk-content
description: The IFaxEventLogging interface defines a configuration object used by a fax client application to configure the event logging categories used by the fax service.
old-location: fax\_mfax_faxeventlogging_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1xt3_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxEventLogging, IFaxEventLogging interface [Fax Service], IFaxEventLogging interface [Fax Service],described, _mfax_faxeventlogging_cpp, fax._mfax_faxeventlogging_cpp, faxcomex/IFaxEventLogging
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
 - IFaxEventLogging
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxEventLogging interface


## -description


The <b>IFaxEventLogging</b> interface defines a configuration object used by a fax client application to configure the event logging categories used by the fax service. You can specify the level of detail at which the fax service logs events in the application log.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxEventLogging</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxEventLogging</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxEventLogging</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686986(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686986(v=VS.85).aspx">IFaxEventLogging::Refresh</a> method refreshes <b>IFaxEventLogging</b> interface information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684805(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684805(v=VS.85).aspx">IFaxEventLogging::Save</a> method saves the <b>IFaxEventLogging</b> interface's data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxEventLogging</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685053(v=VS.85).aspx">GeneralEventsLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685053(v=VS.85).aspx">IFaxEventLogging::get_GeneralEventsLevel</a> property indicates the level of detail at which the fax service logs general events in the application log. General events include those that are not related to initialization and termination or to inbound and outbound transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685116(v=VS.85).aspx">InboundEventsLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685116(v=VS.85).aspx">IFaxEventLogging::get_InboundEventsLevel</a> property indicates the level of detail at which the fax service logs events about inbound fax transmissions in the application log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685042(v=VS.85).aspx">InitEventsLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685042(v=VS.85).aspx">IFaxEventLogging::get_InitEventsLevel</a> property indicates the level of detail at which the fax service logs initialization (starting the server) and termination (shutting down the server) events in the application log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687455(v=VS.85).aspx">OutboundEventsLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687455(v=VS.85).aspx">IFaxEventLogging::get_OutboundEventsLevel</a> property indicates the level of detail at which the fax service logs events about outbound fax transmissions in the application log.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxEventLogging</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms684912(v=VS.85).aspx">FaxEventLogging</a> object.



