---
UID: NN:faxcom.IFaxServer
title: IFaxServer (faxcom.h)
description: The IFaxServer dual interface is used by a fax client application to manage a connection to the fax service.
helpviewer_keywords: ["IFaxServer","IFaxServer interface [Fax Service]","IFaxServer interface [Fax Service]","described","_mfax_ifaxserver_client","fax._mfax_ifaxserver_client","faxcom/IFaxServer"]
old-location: fax\_mfax_ifaxserver_client.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8dx0.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer, IFaxServer interface [Fax Service], IFaxServer interface [Fax Service],described, _mfax_ifaxserver_client, fax._mfax_ifaxserver_client, faxcom/IFaxServer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxServer
 - faxcom/IFaxServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxServer
---

# IFaxServer interface


## -description

The <b>IFaxServer</b> dual interface is used by a fax client application to manage a connection to the fax service. The interface retrieves and sets information about <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> objects; for example, settings for retransmission, branding, archiving and cover pages; discount rate periods; and the status of the fax server queue. The <b>IFaxServer</b> interface includes the following methods:
<ul>
<li>Methods to initiate and terminate connections with a fax server.</li>
<li>Property methods to retrieve and set individual property values of <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> objects. </li>
<li>Methods to create <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs">FaxJobs</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> objects. </li>
</ul><div class="alert"><b>Note</b>  A fax client application must call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to initiate a connection with an active fax server before accessing most interfaces that begin with <b>IFax</b>. (A fax server connection is not required to access an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a> interface.)</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServer</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxServer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxServer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">Connect</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">Connect</a> method connects a fax client application to the specified fax server. Before accessing most interfaces that begin with <b>IFax</b>, the application must call this method to initiate a connection with an active fax server. A fax server connection is not required to access an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-createdocument-vb">CreateDocument</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-createdocument-vb">IFaxServer::CreateDocument</a> method creates a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object for a specified <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The FaxDoc object allows a user to create and transmit a document to one or more fax recipients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">Disconnect</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method terminates a fax client application's connection to a fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getjobs-vb">GetJobs</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getjobs-vb">GetJobs</a> method creates and initializes a <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs-object-visual-basic-">FaxJobs</a> object for a specified <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs">FaxJobs</a> object allows enumeration of the current queued jobs for the connected fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">GetPorts</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">GetPorts</a> method creates and initializes a <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object for a specified <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The FaxPorts object allows enumeration of fax port configuration information for the connected fax server.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-archivedirectory-vb">ArchiveDirectory</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-archivedirectory-vb">IFaxServer::get_ArchiveDirectory</a> method retrieves the <b>ArchiveDirectory</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>ArchiveDirectory</b> property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-archiveoutboundfaxes-vb">ArchiveOutboundFaxes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-archiveoutboundfaxes-vb">ArchiveOutboundFaxes</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>ArchiveOutboundFaxes</b> property is a Boolean value that indicates whether the fax server archives outgoing fax transmissions. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-branding-vb">Branding</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-branding-vb">Branding</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>Branding</b> property is a Boolean value that indicates whether the fax server generates branding information at the top of fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-dirtydays-vb">DirtyDays</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-dirtydays-vb">DirtyDays</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>DirtyDays</b> property is the number of days the fax server retains an unsent job in the fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">DiscountRateEndHour</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendhour-vb">DiscountRateEndHour</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>DiscountRateEndHour</b> property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">DiscountRateEndMinute</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountrateendminute-vb">DiscountRateEndMinute</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>DiscountRateEndMinute</b> property is a number that represents the minute the discount period ends. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">DiscountRateStartHour</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestarthour-vb">DiscountRateStartHour</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>DiscountRateStartHour</b> property is a number that represents the hour the discount period begins. The discount period applies only to outgoing fax transmissions. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">DiscountRateStartMinute</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-discountratestartminute-vb">DiscountRateStartMinute</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>DiscountRateStartMinute</b> property is a number that represents the minute the discount period begins. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-pauseserverqueue-vb">PauseServerQueue</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-pauseserverqueue-vb">PauseServerQueue</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>PauseServerQueue</b> property is a Boolean value that indicates whether the fax server has paused the fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-retries-vb">Retries</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-retries-vb">Retries</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>Retries</b> property is a value that represents the number of times the fax server attempts to retransmit an outgoing fax when the initial transmission fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-retrydelay-vb">RetryDelay</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-retrydelay-vb">RetryDelay</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>RetryDelay</b> property is a value that represents the time interval, in minutes, the fax server waits before attempting to retransmit an outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-servercoverpage-vb">ServerCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-servercoverpage-vb">ServerCoverpage</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>ServerCoverpage</b> property is a Boolean value that indicates whether the fax server permits the use of common cover pages only. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-servermapiprofile-vb">ServerMapiProfile</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-servermapiprofile-vb">ServerMapiProfile</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>ServerMapiProfile</b> property is a null-terminated string that contains the MAPI user profile that the fax server uses for routing incoming fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-usedevicetsid-vb">UseDeviceTsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-get-usedevicetsid-vb">UseDeviceTsid</a> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>UseDeviceTsid</b> property is a Boolean value that indicates whether the fax server uses the device's TSID instead of a user-specified TSID.

</td>
</tr>
</table>

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality.
            

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxServer</b> interface to connect to and disconnect from an active fax server. Also use the interface to retrieve and set the properties of <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxServer</a> objects, and to create the objects listed in the following steps.
			

To connect to a fax server, and create other fax client objects, perform the following steps:

<ol>
<li>Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <b>IFaxServer</b> interface and create an instance of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. </li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to initiate a connection with an active fax server. </li>
<li>After you obtain a connection, call the following methods to create the objects you need: 
<ul>
<li>The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getjobs-vb">IFaxServer::GetJobs</a> method to create a <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs">FaxJobs</a> object. Use this object to create <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> objects and enumerate the fax jobs associated with a connected fax server. </li>
<li>The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">IFaxServer::GetPorts</a> method to create a <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object. Use this object to create <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> objects and enumerate fax port configuration information for a connection to a fax server. </li>
<li>The <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-createdocument-vb">IFaxServer::CreateDocument</a> method to create a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. Use this object to transmit a fax and to retrieve and set the properties of FaxDoc objects. </li>
</ul>
</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each object to allow the object to deallocate itself. Call the method again, if necessary, to destroy the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> or the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a> interface pointers. </li>
</ol>
Note that a client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to create <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs">FaxJobs</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> or <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> objects, or objects derived from these objects. For more information about creating and deallocating fax client objects, see the steps that are listed with each individual interface topic and the hierarchical diagram included in <a href="/previous-versions/windows/desktop/fax/-mfax-the-fax-client-object-model">The Fax Client Object Model</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>