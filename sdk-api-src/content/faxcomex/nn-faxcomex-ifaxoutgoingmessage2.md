---
UID: NN:faxcomex.IFaxOutgoingMessage2
title: IFaxOutgoingMessage2 (faxcomex.h)
author: windows-sdk-content
description: Used by a fax client application to retrieve information about a sent fax message in the archive of outbound faxes.
old-location: fax\_mfax_faxoutgoingmessage2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingmessage2\faxinta_n_ifaxoutgoingmessage2_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessage2, IFaxOutgoingMessage2 interface [Fax Service], IFaxOutgoingMessage2 interface [Fax Service],described, _mfax_faxoutgoingmessage2_cpp, fax._mfax_faxoutgoingmessage2_cpp, faxcomex/IFaxOutgoingMessage2
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
 - IFaxOutgoingMessage2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutgoingMessage2 interface


## -description


Used by a fax client application to retrieve information about a sent fax message in the archive of outbound faxes. The archive contains faxes sent successfully by the fax service. The interface inherits all the functionality of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a> interface. It adds to that information such as whether the fax has a cover page, whether it has been read and what kind of receipt was sent.

The <b>IFaxOutgoingMessage2</b> interface is accessed through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a> interface or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a> interface.


<div class="alert"><b>Note</b>  This interface is supported only on Windows Vista or later.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessage2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>. <b>IFaxOutgoingMessage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutgoingMessage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a> object information from the fax server. When the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-refresh-vb">Refresh</a> method is called, any configuration changes made after the last <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-save-vb">Save</a> method call are lost.



<div class="alert"><b>Note</b>  This method is supported only on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-save-vb">Save</a>
</td>
<td align="left" width="63%">
Saves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a> object's data.



<div class="alert"><b>Note</b>  This method is supported only on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessage2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-hascoverpage-vb">HasCoverPage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates if the fax has a cover page. 



<div class="alert"><b>Note</b>  This property is supported only on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-read-vb">Read</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates if the fax has been read. 



<div class="alert"><b>Note</b>  This property is supported only on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-receiptaddress-vb">ReceiptAddress</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the address to which the delivery report is sent. 



<div class="alert"><b>Note</b>  This property is supported only on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage-receipttype-vb">ReceiptType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the type of delivery report that is sent following an attempted transmission. 



<div class="alert"><b>Note</b>  This property is supported only on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingMessage2</b> object in C++, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxaccountoutgoingarchive-getmessage-vb">IFaxAccountOutgoingArchive::GetMessage</a> method or the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-message">Message</a> method.

A default implementation of this interface is provided by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a> object in Windows Vista or later. The <b>FaxOutgoingMessage</b> object implements the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a> interface on Windows XP or earlier.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccountoutgoingarchive">IFaxAccountOutgoingArchive</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessage">IFaxOutgoingMessage</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingmessageiterator">IFaxOutgoingMessageIterator</a>
 

 

