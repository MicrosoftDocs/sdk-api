---
UID: NN:faxcomex.IFaxOutgoingMessage2
title: IFaxOutgoingMessage2
author: windows-sdk-content
description: Used by a fax client application to retrieve information about a sent fax message in the archive of outbound faxes.
old-location: fax\_mfax_faxoutgoingmessage2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingmessage2\faxinta_n_ifaxoutgoingmessage2_cpp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutgoingMessage2, IFaxOutgoingMessage2 interface [Fax Service], IFaxOutgoingMessage2 interface [Fax Service],described, _mfax_faxoutgoingmessage2_cpp, fax._mfax_faxoutgoingmessage2_cpp, faxcomex/IFaxOutgoingMessage2
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IFaxOutgoingMessage2 interface


## -description


Used by a fax client application to retrieve information about a sent fax message in the archive of outbound faxes. The archive contains faxes sent successfully by the fax service. The interface inherits all the functionality of the <a href="https://msdn.microsoft.com/en-us/library/ms690152(v=VS.85).aspx">IFaxOutgoingMessage</a> interface. It adds to that information such as whether the fax has a cover page, whether it has been read and what kind of receipt was sent.

The <b>IFaxOutgoingMessage2</b> interface is accessed through the <a href="https://msdn.microsoft.com/en-us/library/Aa359025(v=VS.85).aspx">IFaxAccountOutgoingArchive</a> interface or <a href="https://msdn.microsoft.com/en-us/library/ms690096(v=VS.85).aspx">IFaxOutgoingMessageIterator</a> interface.


<div class="alert"><b>Note</b>  This interface is supported only on Windows Vista or later.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessage2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms690152(v=VS.85).aspx">IFaxOutgoingMessage</a>. <b>IFaxOutgoingMessage2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Aa358989(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://msdn.microsoft.com/en-us/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a> object information from the fax server. When the <a href="https://msdn.microsoft.com/en-us/library/Aa358989(v=VS.85).aspx">Refresh</a> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/Aa358990(v=VS.85).aspx">Save</a> method call are lost.



<div class="alert"><b>Note</b>  This method is supported only on Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa358990(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
Saves the <a href="https://msdn.microsoft.com/en-us/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a> object's data.



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

<a href="https://msdn.microsoft.com/en-us/library/Aa358985(v=VS.85).aspx">HasCoverPage</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa358986(v=VS.85).aspx">Read</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa358987(v=VS.85).aspx">ReceiptAddress</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Aa358988(v=VS.85).aspx">ReceiptType</a>


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



To create a <b>FaxIncomingMessage2</b> object in C++, call the <a href="https://msdn.microsoft.com/en-us/library/Aa359026(v=VS.85).aspx">IFaxAccountOutgoingArchive::GetMessage</a> method or the <a href="https://msdn.microsoft.com/en-us/library/ms689615(v=VS.85).aspx">Message</a> method.

A default implementation of this interface is provided by the <a href="https://msdn.microsoft.com/en-us/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a> object in Windows Vista or later. The <b>FaxOutgoingMessage</b> object implements the <a href="https://msdn.microsoft.com/en-us/library/Aa359025(v=VS.85).aspx">IFaxAccountOutgoingArchive</a> interface on Windows XP or earlier.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359025(v=VS.85).aspx">IFaxAccountOutgoingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690152(v=VS.85).aspx">IFaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690096(v=VS.85).aspx">IFaxOutgoingMessageIterator</a>
 

 

