---
UID: NN:faxcomex.IFaxIncomingMessage
title: IFaxIncomingMessage (faxcomex.h)
description: Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes.
old-location: fax\_mfax_faxincomingmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_44h1_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage, IFaxIncomingMessage interface [Fax Service], IFaxIncomingMessage interface [Fax Service],described, _mfax_faxincomingmessage_cpp, fax._mfax_faxincomingmessage_cpp, faxcomex/IFaxIncomingMessage
f1_keywords:
- faxcomex/IFaxIncomingMessage
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
- IFaxIncomingMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingMessage interface


## -description


Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes. The archive contains faxes received successfully by the fax service. The interface also includes methods to delete a message from the archive and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with the fax message to a file on the local computer.

The <b>IFaxIncomingMessage</b> interface is accessed through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a> interface or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessage</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxIncomingMessage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxIncomingMessage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-copytiff-vb">CopyTiff</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-copytiff-vb">CopyTiff</a> method copies the TIFF Class F file associated with the inbound fax message to a file on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-delete-vb">Delete</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-delete-vb">Delete</a> method deletes the specified fax message from the inbound fax archive.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessage</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-callerid-vb">CallerId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-callerid-vb">CallerId</a> property is a null-terminated string that identifies the calling device associated with the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-csid-vb">CSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-csid-vb">CSID</a> property is a null-terminated string that contains the CSID for the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-devicename-vb">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-devicename-vb">DeviceName</a> property is a null-terminated string that contains the name of the device on which the inbound fax message was received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-id-vb">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-id-vb">Id</a> property is a null-terminated string that contains a unique ID for the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-pages-vb">Pages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-pages-vb">Pages</a> property is a value that indicates the total number of pages in the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-retries-vb">Retries</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-retries-vb">Retries</a> property is a value that indicates the number of times that the fax service attempted to route an inbound fax message after the initial routing attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-routinginformation-vb">RoutingInformation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-routinginformation-vb">RoutingInformation</a> property is a null-terminated string that indicates inbound routing information for the fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-size-vb">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-size-vb">Size</a> property is a value that indicates the size of the TIFF Class F file associated with the inbound fax message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-transmissionend-vb">TransmissionEnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-transmissionend-vb">TransmissionEnd</a> property indicates the time that the inbound fax message completed transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-transmissionstart-vb">TransmissionStart</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-transmissionstart-vb">TransmissionStart</a> property indicates the time that the inbound fax message began transmitting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-tsid-vb">TSID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage-tsid-vb">TSID</a> property is a null-terminated string that contains the TSID associated with the inbound fax message.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingMessage</b> object in C++, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingarchive-getmessage-vb">IFaxIncomingArchive::GetMessage</a> method or the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessageiterator-message-vb">IFaxIncomingMessageIterator::get_Message</a> method.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingmessage">FaxIncomingMessage</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingarchive">IFaxIncomingArchive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxincomingmessageiterator">IFaxIncomingMessageIterator</a>
 

 

