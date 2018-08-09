---
UID: NN:faxcomex.IFaxActivityLogging
title: IFaxActivityLogging
author: windows-sdk-content
description: The IFaxActivityLogging interface defines a configuration object used by a fax client application to retrieve and set options for activity logging.
old-location: fax\_mfax_faxactivitylogging_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0odj_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxActivityLogging, IFaxActivityLogging interface [Fax Service], IFaxActivityLogging interface [Fax Service],described, _mfax_faxactivitylogging_cpp, fax._mfax_faxactivitylogging_cpp, faxcomex/IFaxActivityLogging
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
 - IFaxActivityLogging
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxActivityLogging interface


## -description


The <b>IFaxActivityLogging</b> interface defines a configuration object used by a fax client application to retrieve and set options for activity logging. This includes setting whether entries for incoming and outgoing faxes should be logged and the location of the log file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxActivityLogging</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxActivityLogging</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxActivityLogging</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684842(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684842(v=VS.85).aspx">IFaxActivityLogging::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms684576(v=VS.85).aspx">FaxActivityLogging</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685941(v=VS.85).aspx">IFaxActivityLogging::Save</a> method saves the <a href="https://msdn.microsoft.com/en-us/library/ms684576(v=VS.85).aspx">FaxActivityLogging</a> object's data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxActivityLogging</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687463(v=VS.85).aspx">DatabasePath</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687463(v=VS.85).aspx">IFaxActivityLogging::get_DatabasePath</a> property is a null-terminated string that contains the path to the activity log database file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686023(v=VS.85).aspx">LogIncoming</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686023(v=VS.85).aspx">IFaxActivityLogging::get_LogIncoming</a> property is a Boolean value that indicates whether the fax service logs entries for incoming faxes in the activity log database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686497(v=VS.85).aspx">LogOutgoing</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686497(v=VS.85).aspx">IFaxActivityLogging::get_LogOutgoing</a> property is a Boolean value that indicates whether the fax service logs entries for outgoing faxes in the activity log database.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxActivityLogging</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms684576(v=VS.85).aspx">FaxActivityLogging</a> object.



