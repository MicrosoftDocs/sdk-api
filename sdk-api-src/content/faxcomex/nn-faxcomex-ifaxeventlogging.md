---
UID: NN:faxcomex.IFaxEventLogging
title: IFaxEventLogging
author: windows-sdk-content
description: The IFaxEventLogging interface defines a configuration object used by a fax client application to configure the event logging categories used by the fax service.
old-location: fax\_mfax_faxeventlogging_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1xt3_cpp.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IFaxEventLogging, IFaxEventLogging interface [Fax Service], IFaxEventLogging interface [Fax Service],described, _mfax_faxeventlogging_cpp, fax._mfax_faxeventlogging_cpp, faxcomex/IFaxEventLogging
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxEventLogging interface


## -description


The <b>IFaxEventLogging</b> interface defines a configuration object used by a fax client application to configure the event logging categories used by the fax service. You can specify the level of detail at which the fax service logs events in the application log.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxEventLogging</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxEventLogging</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f7ccdd18-3287-49fd-aa2a-5a713da44877">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f7ccdd18-3287-49fd-aa2a-5a713da44877">IFaxEventLogging::Refresh</a> method refreshes <b>IFaxEventLogging</b> interface information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/04783d57-a568-4848-b563-a8ef8544089d">IFaxEventLogging::Save</a> method saves the <b>IFaxEventLogging</b> interface's data.

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

<a href="https://msdn.microsoft.com/8ab80241-44ab-49e3-97b9-d4c0e8cfa096">GeneralEventsLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8ab80241-44ab-49e3-97b9-d4c0e8cfa096">IFaxEventLogging::get_GeneralEventsLevel</a> property indicates the level of detail at which the fax service logs general events in the application log. General events include those that are not related to initialization and termination or to inbound and outbound transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aa223f94-cc2b-4704-9b57-22e1cb7d1a89">InboundEventsLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/aa223f94-cc2b-4704-9b57-22e1cb7d1a89">IFaxEventLogging::get_InboundEventsLevel</a> property indicates the level of detail at which the fax service logs events about inbound fax transmissions in the application log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5a8f73d1-c612-4589-91bc-84a4659faefd">InitEventsLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5a8f73d1-c612-4589-91bc-84a4659faefd">IFaxEventLogging::get_InitEventsLevel</a> property indicates the level of detail at which the fax service logs initialization (starting the server) and termination (shutting down the server) events in the application log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/115e661c-4f44-4ed3-a591-ffa89d55d72b">OutboundEventsLevel</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/115e661c-4f44-4ed3-a591-ffa89d55d72b">IFaxEventLogging::get_OutboundEventsLevel</a> property indicates the level of detail at which the fax service logs events about outbound fax transmissions in the application log.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxEventLogging</b> is provided as the <a href="https://msdn.microsoft.com/library/ms684912(v=VS.85).aspx">FaxEventLogging</a> object.



