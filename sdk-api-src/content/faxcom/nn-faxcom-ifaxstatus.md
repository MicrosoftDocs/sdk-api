---
UID: NN:faxcom.IFaxStatus
title: IFaxStatus (faxcom.h)
author: windows-sdk-content
description: The FaxStatus dual interface is used by a fax client application to retrieve status information for a specific port on a connected fax server.
old-location: fax\_mfax_ifaxstatus.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0ckz.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxStatus, IFaxStatus interface [Fax Service], IFaxStatus interface [Fax Service],described, _mfax_ifaxstatus, fax._mfax_ifaxstatus, faxcom/IFaxStatus
ms.topic: interface
f1_keywords: 
 - "faxcom/IFaxStatus"
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxStatus interface


## -description


The <b>FaxStatus</b> dual interface is used by a fax client application to retrieve status information for a specific port on a connected fax server. The <b>IFaxStatus</b> interface includes the following interface methods:
<ul>
<li>A method to update status information for a fax port. </li>
<li>Property methods to retrieve attributes of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object, such as whether the parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> is currently sending or receiving a fax transmission. Attributes also include document and transmission data, sender and recipient names, and routing information. </li>
</ul>

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object should only be created by a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. 




You can use the FaxStatus object to provide real-time status information about a parent FaxPort object. Some data is available at all times for an active fax port; other data is relative to sending or receiving a fax and is only available at those times.

		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxStatus</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-refresh-vb">Refresh</a> method updates <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object information for the associated parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxStatus</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-address-vb">Address</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-address-vb">Address</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Address</b> property is a null-terminated string that contains the destination of a fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-callerid-vb">CallerId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-callerid-vb">CallerId</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>CallerId</b> property is a string that identifies the calling device that sent an inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-csid-vb">Csid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-csid-vb">Csid</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Csid</b> property is a string that contains CSID information, typically the fax number of the receiving device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-currentpage-vb">CurrentPage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-currentpage-vb">CurrentPage</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>CurrentPage</b> property is a number that identifies the current page of an active outbound fax job on a specific port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-description-vb">Description</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-description-vb">Description</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Description</b> property is a null-terminated string that describes the current status of the specified port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-deviceid-vb">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-deviceid-vb">DeviceId</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>DeviceId</b> property is a number representing the permanent line identifier for the fax port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-devicename-vb">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-devicename-vb">DeviceName</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>DeviceName</b> property is a null-terminated string that contains the user-friendly display name for the fax port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-documentname-vb">DocumentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-documentname-vb">DocumentName</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>DocumentName</b> property is a null-terminated string that contains the user-friendly name associated with an active fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-documentsize-vb">DocumentSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-documentsize-vb">DocumentSize</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>DocumentSize</b> property is the size of the fax document associated with the active outbound job on a specific port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-elapsedtime-vb">ElapsedTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-elapsedtime-vb">ElapsedTime</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>ElapsedTime</b> property is a number that represents the elapsed time for an active fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-pagecount-vb">PageCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-pagecount-vb">PageCount</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>PageCount</b> property represents the total number of pages in an outbound fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-receive-vb">Receive</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-receive-vb">Receive</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Receive</b> property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-recipientname-vb">RecipientName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-recipientname-vb">RecipientName</a> property for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient of an inbound fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-routingstring-vb">RoutingString</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-routingstring-vb">RoutingString</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>RoutingString</b> property is a null-terminated string that contains routing information for inbound fax transmissions that is specific to a fax service provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-send-vb">Send</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-send-vb">Send</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Send</b> property is a Boolean value that indicates whether a specified fax port is currently sending a fax. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-sendername-vb">SenderName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-sendername-vb">SenderName</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the user who sent the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-starttime-vb">StartTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-starttime-vb">StartTime</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>StartTime</b> property is a number that represents the starting time for an active fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-submittedtime-vb">SubmittedTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-submittedtime-vb">SubmittedTime</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>SubmittedTime</b> property is a number that represents the time the user submitted the active fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-tsid-vb">Tsid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxstatus-get-tsid-vb">Tsid</a> property for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object of a parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The <b>Tsid</b> property is a null-terminated string that contains the TSID associated with the fax port.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality.
            

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxStatus</b> interface to update the status information for a specific fax port, and to retrieve the properties of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. 





A client application should not call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <b>IFaxStatus</b> interface pointer. Instead, the application must perform the following steps to create an instance of a FaxStatus object: 


<ol>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface. </li>
<li>Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">IFaxServer::GetPorts</a> method to create and initialize a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object for the connected fax server. </li>
<li>Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_count">IFaxPorts::get_Count</a> method and then the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_item">IFaxPorts::get_Item</a> method to retrieve <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointers for each child <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. (You can also call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a> method to retrieve an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a> interface pointer.) </li>
<li>Use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxport-getstatus-vb">IFaxPort::GetStatus</a> interface method, to retrieve an IDispatch interface pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. </li>
<li>Use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call <b>IFaxStatus</b> interface methods. </li>
<li>Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server. </li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object to allow the object to deallocate itself. Also call IUnknown::Release once for each <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object, and again to destroy both the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> and the parent <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface pointers. </li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

