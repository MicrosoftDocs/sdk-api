---
UID: NN:faxcomex.IFaxAccount
title: IFaxAccount
author: windows-sdk-content
description: Represents a fax account on the fax server.
old-location: fax\_mfax_faxaccount_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccount\faxinta_n_ifaxaccount.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxAccount, IFaxAccount interface [Fax Service], IFaxAccount interface [Fax Service],described, _mfax_faxaccount_cpp, fax._mfax_faxaccount_cpp, faxcomex/IFaxAccount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxAccount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccount interface


## -description


Represents a <a href="https://msdn.microsoft.com/en-us/library/Aa358860(v=VS.85).aspx">fax account</a> on the fax server.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccount</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxAccount</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxAccount</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359060(v=VS.85).aspx">ListenToAccountEvents</a>
</td>
<td align="left" width="63%">
Sets the flags of a <a href="https://msdn.microsoft.com/en-us/library/Aa359063(v=VS.85).aspx">FAX_ACCOUNT_EVENTS_TYPE_ENUM</a> variable that represents the events for which the account is listening.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccount</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa359057(v=VS.85).aspx">AccountName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of a particular fax account on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa359059(v=VS.85).aspx">Folders</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Represents the folders of the account, including the incoming and outgoing archives and the incoming and outgoing queues.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa359061(v=VS.85).aspx">RegisteredEvents</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A set of flags indicating the type of events for which the account is listening.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxAccount</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/Aa358967(v=VS.85).aspx">FaxAccount</a> object. The interface and the object are supported only on Windows Vista or later.



