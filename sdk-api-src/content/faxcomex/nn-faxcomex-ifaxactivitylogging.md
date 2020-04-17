---
UID: NN:faxcomex.IFaxActivityLogging
title: IFaxActivityLogging (faxcomex.h)
description: The IFaxActivityLogging interface defines a configuration object used by a fax client application to retrieve and set options for activity logging.helpviewer_keywords: ["IFaxActivityLogging","IFaxActivityLogging interface [Fax Service]","IFaxActivityLogging interface [Fax Service]","described","_mfax_faxactivitylogging_cpp","fax._mfax_faxactivitylogging_cpp","faxcomex/IFaxActivityLogging"]
old-location: fax\_mfax_faxactivitylogging_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0odj_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivityLogging, IFaxActivityLogging interface [Fax Service], IFaxActivityLogging interface [Fax Service],described, _mfax_faxactivitylogging_cpp, fax._mfax_faxactivitylogging_cpp, faxcomex/IFaxActivityLogging
f1_keywords:
- faxcomex/IFaxActivityLogging
dev_langs:
- c++
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
- IFaxActivityLogging
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxActivityLogging interface


## -description


The <b>IFaxActivityLogging</b> interface defines a configuration object used by a fax client application to retrieve and set options for activity logging. This includes setting whether entries for incoming and outgoing faxes should be logged and the location of the log file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxActivityLogging</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxActivityLogging</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-refresh-vb">IFaxActivityLogging::Refresh</a> method refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-save-vb">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-save-vb">IFaxActivityLogging::Save</a> method saves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> object's data.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-databasepath-vb">DatabasePath</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-databasepath-vb">IFaxActivityLogging::get_DatabasePath</a> property is a null-terminated string that contains the path to the activity log database file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-logincoming-vb">LogIncoming</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-logincoming-vb">IFaxActivityLogging::get_LogIncoming</a> property is a Boolean value that indicates whether the fax service logs entries for incoming faxes in the activity log database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-logoutgoing-vb">LogOutgoing</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging-logoutgoing-vb">IFaxActivityLogging::get_LogOutgoing</a> property is a Boolean value that indicates whether the fax service logs entries for outgoing faxes in the activity log database.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxActivityLogging</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a> object.



