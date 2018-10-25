---
UID: NN:faxcomex.IFaxDocument
title: IFaxDocument
author: windows-sdk-content
description: The IFaxDocument interface defines a messaging object used by a fax client application to compose a fax document and submit it to the fax service for processing.
old-location: fax\_mfax_faxdocument_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_3md0_cpp.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxDocument, IFaxDocument interface [Fax Service], IFaxDocument interface [Fax Service],described, _mfax_faxdocument_cpp, fax._mfax_faxdocument_cpp, faxcomex/IFaxDocument
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
 - IFaxDocument
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDocument interface


## -description


The <b>IFaxDocument</b> interface defines a messaging object used by a fax client application to compose a fax document and submit it to the fax service for processing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDocument</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxDocument</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxDocument</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686179(v=VS.85).aspx">ConnectedSubmit</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686179(v=VS.85).aspx">IFaxDocument::ConnectedSubmit</a> method submits a single fax document to the connected <a href="https://msdn.microsoft.com/en-us/library/ms689110(v=VS.85).aspx">IFaxServer</a>. The method returns an array of fax job ID strings, one for each recipient of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687477(v=VS.85).aspx">Submit</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687477(v=VS.85).aspx">IFaxDocument::Submit</a> method submits a single fax document to the fax service for processing.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDocument</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686176(v=VS.85).aspx">AttachFaxToReceipt</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686176(v=VS.85).aspx">IFaxDocument::get_AttachFaxToReceipt</a> property indicates whether to attach a fax to the receipt.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684817(v=VS.85).aspx">Body</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684817(v=VS.85).aspx">IFaxDocument::get_Body</a> property provides the path to the file that comprises the body of a fax. The body of a fax consists of the fax pages other than the cover page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687493(v=VS.85).aspx">CoverPage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687493(v=VS.85).aspx">IFaxDocument::get_CoverPage</a> property is a null-terminated string that contains the name of the cover page template file (.cov) to associate with the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686003(v=VS.85).aspx">CoverPageType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686003(v=VS.85).aspx">IFaxDocument::get_CoverPageType</a> property is a value from an enumeration that indicates whether a specified cover page template file (.cov) is a server-based cover page file or a local-computer-based cover page file. You can also specify that no file is used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685139(v=VS.85).aspx">DocumentName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685139(v=VS.85).aspx">IFaxDocument::get_DocumentName</a> property is a null-terminated string that contains the user-friendly name to display for the fax document. The value is for display purposes only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685135(v=VS.85).aspx">GroupBroadcastReceipts</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685135(v=VS.85).aspx">IFaxDocument::get_GroupBroadcastReceipts</a> property is a Boolean value that indicates whether to send an individual delivery receipt for each recipient of the broadcast, or to send a summary receipt for all the recipients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687453(v=VS.85).aspx">Note</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687453(v=VS.85).aspx">IFaxDocument::get_Note</a> property is a null-terminated string that contains the contents of the note field on the cover page of the fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687026(v=VS.85).aspx">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687026(v=VS.85).aspx">IFaxDocument::get_Priority</a> property specifies the priority to use when sending the fax; for example, normal, low, or high priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687514(v=VS.85).aspx">ReceiptAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687514(v=VS.85).aspx">IFaxDocument::get_ReceiptAddress</a> property is a null-terminated string that indicates the email address to which the fax service should send a delivery receipt when the fax job reaches a final state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686899(v=VS.85).aspx">ReceiptType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686899(v=VS.85).aspx">IFaxDocument::get_ReceiptType</a> property specifies the type of delivery receipt to deliver when the fax job reaches a final state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687440(v=VS.85).aspx">Recipients</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687440(v=VS.85).aspx">IFaxDocument::get_Recipients</a> property retrieves a collection of one or more recipients for the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686129(v=VS.85).aspx">ScheduleTime</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686129(v=VS.85).aspx">IFaxDocument::get_ScheduleTime</a> property indicates the time to submit the fax for processing to the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686190(v=VS.85).aspx">ScheduleType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686190(v=VS.85).aspx">IFaxDocument::get_ScheduleType</a> property indicates when to schedule the fax job; for example, you can specify that the fax service send the fax immediately, at a specified time, or during a predefined discount period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685034(v=VS.85).aspx">Sender</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an object containing information about the sender of the fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685109(v=VS.85).aspx">Subject</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685109(v=VS.85).aspx">IFaxDocument::get_Subject</a> property is a null-terminated string that contains the contents of the subject field on the cover page of the fax.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxDocument</b> and <a href="https://msdn.microsoft.com/en-us/library/Aa359010(v=VS.85).aspx">IFaxDocument2</a> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms685958(v=VS.85).aspx">FaxDocument</a> object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685958(v=VS.85).aspx">FaxDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

