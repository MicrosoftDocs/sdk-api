---
UID: NN:faxcomex.IFaxAccountIncomingArchive
title: IFaxAccountIncomingArchive (faxcomex.h)
author: windows-sdk-content
description: Used by a fax client application to access a particular fax account's archive of successfully received inbound fax messages. Use this interface to retrieve messages and get the size of the archive.
old-location: fax\_mfax_faxaccountincomingarchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\faxint_ifaxaccountincomingarchive.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxAccountIncomingArchive, IFaxAccountIncomingArchive interface [Fax Service], IFaxAccountIncomingArchive interface [Fax Service],described, _mfax_faxaccountincomingarchive_cpp, fax._mfax_faxaccountincomingarchive_cpp, faxcomex/IFaxAccountIncomingArchive
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
 - IFaxAccountIncomingArchive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxAccountIncomingArchive interface


## -description


Used by a fax client application to access a particular fax account's archive of successfully received inbound fax messages. Use this interface to retrieve messages and get the size of the archive.

A default implementation of <b>IFaxAccountIncomingArchive</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/Aa358957(v=VS.85).aspx">FaxAccountIncomingArchive</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountIncomingArchive</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxAccountIncomingArchive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxAccountIncomingArchive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359047(v=VS.85).aspx">GetMessage</a>
</td>
<td align="left" width="63%">
Returns a fax message from the archive of inbound faxes, for a particular fax account, by using the fax message ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359048(v=VS.85).aspx">GetMessages</a>
</td>
<td align="left" width="63%">
Returns a new iterator (archive cursor) for the archive of inbound fax messages for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa359049(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://msdn.microsoft.com/en-us/library/Aa358957(v=VS.85).aspx">FaxAccountIncomingArchive</a> object information for a particular fax account from the fax server. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxAccountIncomingArchive</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa359050(v=VS.85).aspx">SizeHigh</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the high 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa359051(v=VS.85).aspx">SizeLow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358957(v=VS.85).aspx">FaxAccountIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

