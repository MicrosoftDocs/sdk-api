---
UID: NN:faxcomex.IFaxAccountOutgoingArchive
title: IFaxAccountOutgoingArchive
author: windows-sdk-content
description: Used by a fax client application to access a specified fax account's archive of successfully sent outbound fax messages. Use this interface to retrieve messages and get the size of the archive.
old-location: fax\_mfax_faxaccountoutgoingarchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountoutgoingarchive\faxint_ifaxaccountoutgoingarchive.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxAccountOutgoingArchive, IFaxAccountOutgoingArchive interface [Fax Service], IFaxAccountOutgoingArchive interface [Fax Service],described, _mfax_faxaccountoutgoingarchive_cpp, fax._mfax_faxaccountoutgoingarchive_cpp, faxcomex/IFaxAccountOutgoingArchive
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
 - IFaxAccountOutgoingArchive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountOutgoingArchive interface


## -description


Used by a fax client application to access a specified fax account's archive of successfully sent outbound fax messages. Use this interface to retrieve messages and get the size of the archive.

A default implementation of <b>IFaxAccountOutgoingArchive</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/Aa358948(v=VS.85).aspx">FaxAccountOutgoingArchive</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountOutgoingArchive</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxAccountOutgoingArchive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxAccountOutgoingArchive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359026(v=VS.85).aspx">GetMessage</a>
</td>
<td align="left" width="63%">
Returns a fax message from the archive of outbound faxes for a particular fax account, by using the fax message ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359027(v=VS.85).aspx">GetMessages</a>
</td>
<td align="left" width="63%">
Returns a new iterator (archive cursor) for the archive of outbound fax messages for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359028(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://msdn.microsoft.com/en-us/library/Aa358948(v=VS.85).aspx">FaxAccountOutgoingArchive</a> object information for a particular fax account from the fax server. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountOutgoingArchive</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa359029(v=VS.85).aspx">SizeHigh</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the high-order 32-bit value of the size (in bytes) of the archive of outbound fax messages for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa359030(v=VS.85).aspx">SizeLow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the low-order 32-bit value of the size (in bytes) of the archive of outbound fax messages for a particular fax account.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358948(v=VS.85).aspx">FaxAccountOutgoingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

