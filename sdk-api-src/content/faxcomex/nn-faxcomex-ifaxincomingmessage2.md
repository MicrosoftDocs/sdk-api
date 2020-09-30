---
UID: NN:faxcomex.IFaxIncomingMessage2
title: IFaxIncomingMessage2 (faxcomex.h)
description: Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes.
helpviewer_keywords: ["IFaxIncomingMessage2","IFaxIncomingMessage2 interface [Fax Service]","IFaxIncomingMessage2 interface [Fax Service]","described","_mfax_faxincomingmessage2_cpp","fax._mfax_faxincomingmessage2_cpp","faxcomex/IFaxIncomingMessage2"]
old-location: fax\_mfax_faxincomingmessage2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\faxinta_n_ifaxincomingmessage2_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage2, IFaxIncomingMessage2 interface [Fax Service], IFaxIncomingMessage2 interface [Fax Service],described, _mfax_faxincomingmessage2_cpp, fax._mfax_faxincomingmessage2_cpp, faxcomex/IFaxIncomingMessage2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxIncomingMessage2
 - faxcomex/IFaxIncomingMessage2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingMessage2
---

# IFaxIncomingMessage2 interface


## -description

Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes. The archive contains faxes received successfully by the fax service. The interface also includes methods to delete a message from the archive and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with the fax message to a file on the local computer.

The <b>IFaxIncomingMessage2</b> interface is accessed through the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountincomingarchive">IFaxAccountIncomingArchive</a> interface or <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessage2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingMessage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxIncomingMessage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-reassign-vb">Reassign</a>
</td>
<td align="left" width="63%">

<a href="/previous-versions/windows/desktop/fax/-mfax-glossary">Reassign</a> the fax to one or more recipients. It also commits changes to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-subject-vb">IFaxIncomingMessage2::Subject</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-sendername-vb">IFaxIncomingMessage2::SenderName</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-senderfaxnumber-vb">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-hascoverpage-vb">IFaxIncomingMessage2::HasCoverPage</a> properties.



<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a> object information from the fax server. When the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-refresh-vb">Refresh</a> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-save-vb">Save</a> method call are lost, except for the properties that are committed with the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-reassign-vb">IFaxIncomingMessage2::Reassign</a> method: <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-subject-vb">IFaxIncomingMessage2::Subject</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-sendername-vb">IFaxIncomingMessage2::SenderName</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-senderfaxnumber-vb">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-hascoverpage-vb">IFaxIncomingMessage2::HasCoverPage</a>.



<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-save-vb">Save</a>
</td>
<td align="left" width="63%">
Saves the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a> object's data.



<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessage2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-hascoverpage-vb">HasCoverPage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
A flag that indicates whether the fax has a cover page. 



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-read-vb">Read</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
A flag that indicates if the fax has been read. 



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-recipients-vb">Recipients</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Contains the recipients associated with the inbound fax message. This property is a null-terminated string.



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-senderfaxnumber-vb">SenderFaxNumber</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Contains the sender's fax number associated with the inbound fax message. This property is a null-terminated string. 



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-sendername-vb">SenderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Contains the name of the sender that is associated with the inbound fax message. This property is a null-terminated string.



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-subject-vb">Subject</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-subject-vb">Subject</a> property contains the subject associated with the inbound fax message. This property is a null-terminated string.



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-wasreassigned-vb">WasReAssigned</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates if the fax has been reassigned. 

<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
</table>

## -remarks

To create a <b>FaxIncomingMessage2</b> object in C++, call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">IFaxAccountIncomingArchive::GetMessage</a> method or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator-message-vb">IFaxIncomingMessageIterator::get_Message</a> method.

A default implementation of this interface is provided by the <a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountincomingarchive">IFaxAccountIncomingArchive</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a>