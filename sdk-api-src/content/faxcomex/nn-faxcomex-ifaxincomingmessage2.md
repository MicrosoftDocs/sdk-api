---
UID: NN:faxcomex.IFaxIncomingMessage2
title: IFaxIncomingMessage2
author: windows-sdk-content
description: Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes.
old-location: fax\_mfax_faxincomingmessage2_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\faxinta_n_ifaxincomingmessage2_cpp.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxIncomingMessage2, IFaxIncomingMessage2 interface [Fax Service], IFaxIncomingMessage2 interface [Fax Service],described, _mfax_faxincomingmessage2_cpp, fax._mfax_faxincomingmessage2_cpp, faxcomex/IFaxIncomingMessage2
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxIncomingMessage2
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingMessage2 interface


## -description


Used by a fax client application to retrieve information about a received fax message in the archive of inbound faxes. The archive contains faxes received successfully by the fax service. The interface also includes methods to delete a message from the archive and to copy the Tagged Image File Format Class F (TIFF Class F) file associated with the fax message to a file on the local computer.

The <b>IFaxIncomingMessage2</b> interface is accessed through the <a href="https://msdn.microsoft.com/8a10e18a-fed1-47b0-bb5b-b9f21f234c5b">IFaxAccountIncomingArchive</a> interface or <a href="https://msdn.microsoft.com/f0b3071b-6936-4b19-873b-0ab28cfaea93">IFaxIncomingMessageIterator</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessage2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxIncomingMessage2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/befff3bc-4489-4a63-b231-ff2974c760d1">Reassign</a>
</td>
<td align="left" width="63%">

<a href="https://msdn.microsoft.com/ede1c31f-e53a-4ddc-ba25-6fcadadd513a">Reassign</a> the fax to one or more recipients. It also commits changes to the <a href="https://msdn.microsoft.com/b6722c85-3750-4a5d-baf0-05c7f79c45af">IFaxIncomingMessage2::Subject</a>, <a href="https://msdn.microsoft.com/dba0099d-bf47-47e0-8a83-39a2fe9f4793">IFaxIncomingMessage2::SenderName</a>, <a href="https://msdn.microsoft.com/304f722e-4ea6-472c-99c3-1b129d143dae">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="https://msdn.microsoft.com/71bd6223-e5d3-453c-b747-9b0be9b074c6">IFaxIncomingMessage2::HasCoverPage</a> properties.



<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6f15a7d-7018-427a-9069-182764165cfd">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a> object information from the fax server. When the <a href="https://msdn.microsoft.com/a6f15a7d-7018-427a-9069-182764165cfd">Refresh</a> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a> method call are lost, except for the properties that are committed with the <a href="https://msdn.microsoft.com/befff3bc-4489-4a63-b231-ff2974c760d1">IFaxIncomingMessage2::Reassign</a> method: <a href="https://msdn.microsoft.com/b6722c85-3750-4a5d-baf0-05c7f79c45af">IFaxIncomingMessage2::Subject</a>, <a href="https://msdn.microsoft.com/dba0099d-bf47-47e0-8a83-39a2fe9f4793">IFaxIncomingMessage2::SenderName</a>, <a href="https://msdn.microsoft.com/304f722e-4ea6-472c-99c3-1b129d143dae">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="https://msdn.microsoft.com/71bd6223-e5d3-453c-b747-9b0be9b074c6">IFaxIncomingMessage2::HasCoverPage</a>.



<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
Saves the <a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a> object's data.



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

<a href="https://msdn.microsoft.com/71bd6223-e5d3-453c-b747-9b0be9b074c6">HasCoverPage</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>


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

<a href="https://msdn.microsoft.com/72dac889-f119-4da7-835b-c0725921cf57">Recipients</a>


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

<a href="https://msdn.microsoft.com/304f722e-4ea6-472c-99c3-1b129d143dae">SenderFaxNumber</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/mt764038">SenderName</a>


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

<a href="https://msdn.microsoft.com/b6722c85-3750-4a5d-baf0-05c7f79c45af">Subject</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b6722c85-3750-4a5d-baf0-05c7f79c45af">Subject</a> property contains the subject associated with the inbound fax message. This property is a null-terminated string.



<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c7318bec-320f-484e-a3d0-61f5d4422784">WasReAssigned</a>


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



To create a <b>FaxIncomingMessage2</b> object in C++, call the <a href="https://msdn.microsoft.com/f9e253ef-1f61-48d5-9f71-7e14ebf538fa">IFaxAccountIncomingArchive::GetMessage</a> method or the <a href="https://msdn.microsoft.com/52846cf4-4e6b-43cc-a9ba-3e4820fc2aa8">IFaxIncomingMessageIterator::get_Message</a> method.

A default implementation of this interface is provided by the <a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a> object.




## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/8a10e18a-fed1-47b0-bb5b-b9f21f234c5b">IFaxAccountIncomingArchive</a>



<a href="https://msdn.microsoft.com/f0b3071b-6936-4b19-873b-0ab28cfaea93">IFaxIncomingMessageIterator</a>
 

 

