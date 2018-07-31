---
UID: NN:faxcom.IFaxServer
title: IFaxServer
author: windows-sdk-content
description: The IFaxServer dual interface is used by a fax client application to manage a connection to the fax service.
old-location: fax\_mfax_ifaxserver_client.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8dx0.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IFaxServer, IFaxServer interface [Fax Service], IFaxServer interface [Fax Service],described, _mfax_ifaxserver_client, fax._mfax_ifaxserver_client, faxcom/IFaxServer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxServer
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer interface


## -description


The <b>IFaxServer</b> dual interface is used by a fax client application to manage a connection to the fax service. The interface retrieves and sets information about <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> objects; for example, settings for retransmission, branding, archiving and cover pages; discount rate periods; and the status of the fax server queue. The <b>IFaxServer</b> interface includes the following methods:
<ul>
<li>Methods to initiate and terminate connections with a fax server.</li>
<li>Property methods to retrieve and set individual property values of <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> objects. </li>
<li>Methods to create <a href="https://msdn.microsoft.com/library/ms692796(v=VS.85).aspx">FaxJobs</a>, <a href="https://msdn.microsoft.com/library/ms692319(v=VS.85).aspx">FaxPorts</a> and <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> objects. </li>
</ul><div class="alert"><b>Note</b>  A fax client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">IFaxServer::Connect</a> method to initiate a connection with an active fax server before accessing most interfaces that begin with <b>IFax</b>. (A fax server connection is not required to access an <a href="https://msdn.microsoft.com/library/ms691802(v=VS.85).aspx">IFaxTiff</a> interface.)</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServer</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxServer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">Connect</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">Connect</a> method connects a fax client application to the specified fax server. Before accessing most interfaces that begin with <b>IFax</b>, the application must call this method to initiate a connection with an active fax server. A fax server connection is not required to access an <a href="https://msdn.microsoft.com/library/ms691802(v=VS.85).aspx">IFaxTiff</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms690786(v=VS.85).aspx">CreateDocument</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690786(v=VS.85).aspx">IFaxServer::CreateDocument</a> method creates a <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> object for a specified <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The FaxDoc object allows a user to create and transmit a document to one or more fax recipients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms691936(v=VS.85).aspx">Disconnect</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691936(v=VS.85).aspx">IFaxServer::Disconnect</a> method terminates a fax client application's connection to a fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms692836(v=VS.85).aspx">GetJobs</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692836(v=VS.85).aspx">GetJobs</a> method creates and initializes a <a href="https://msdn.microsoft.com/library/ms690701(v=VS.85).aspx">FaxJobs</a> object for a specified <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <a href="https://msdn.microsoft.com/library/ms692796(v=VS.85).aspx">FaxJobs</a> object allows enumeration of the current queued jobs for the connected fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms692815(v=VS.85).aspx">GetPorts</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692815(v=VS.85).aspx">GetPorts</a> method creates and initializes a <a href="https://msdn.microsoft.com/library/ms692319(v=VS.85).aspx">FaxPorts</a> object for a specified <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The FaxPorts object allows enumeration of fax port configuration information for the connected fax server.

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

<a href="https://msdn.microsoft.com/en-us/library/ms691828(v=VS.85).aspx">ArchiveDirectory</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691828(v=VS.85).aspx">IFaxServer::get_ArchiveDirectory</a> method retrieves the <b>ArchiveDirectory</b> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>ArchiveDirectory</b> property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692347(v=VS.85).aspx">ArchiveOutboundFaxes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692347(v=VS.85).aspx">ArchiveOutboundFaxes</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>ArchiveOutboundFaxes</b> property is a Boolean value that indicates whether the fax server archives outgoing fax transmissions. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690912(v=VS.85).aspx">Branding</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690912(v=VS.85).aspx">Branding</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>Branding</b> property is a Boolean value that indicates whether the fax server generates branding information at the top of fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691836(v=VS.85).aspx">DirtyDays</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691836(v=VS.85).aspx">DirtyDays</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>DirtyDays</b> property is the number of days the fax server retains an unsent job in the fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691317(v=VS.85).aspx">DiscountRateEndHour</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691317(v=VS.85).aspx">DiscountRateEndHour</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>DiscountRateEndHour</b> property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690899(v=VS.85).aspx">DiscountRateEndMinute</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">

		Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690899(v=VS.85).aspx">DiscountRateEndMinute</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>DiscountRateEndMinute</b> property is a number that represents the minute the discount period ends. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">

		Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>DiscountRateStartHour</b> property is a number that represents the hour the discount period begins. The discount period applies only to outgoing fax transmissions. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>DiscountRateStartMinute</b> property is a number that represents the minute the discount period begins. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692825(v=VS.85).aspx">PauseServerQueue</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692825(v=VS.85).aspx">PauseServerQueue</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>PauseServerQueue</b> property is a Boolean value that indicates whether the fax server has paused the fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691491(v=VS.85).aspx">Retries</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691491(v=VS.85).aspx">Retries</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>Retries</b> property is a value that represents the number of times the fax server attempts to retransmit an outgoing fax when the initial transmission fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691953(v=VS.85).aspx">RetryDelay</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691953(v=VS.85).aspx">RetryDelay</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>RetryDelay</b> property is a value that represents the time interval, in minutes, the fax server waits before attempting to retransmit an outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691428(v=VS.85).aspx">ServerCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms691428(v=VS.85).aspx">ServerCoverpage</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>ServerCoverpage</b> property is a Boolean value that indicates whether the fax server permits the use of common cover pages only. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692833(v=VS.85).aspx">ServerMapiProfile</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms692833(v=VS.85).aspx">ServerMapiProfile</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>ServerMapiProfile</b> property is a null-terminated string that contains the MAPI user profile that the fax server uses for routing incoming fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690868(v=VS.85).aspx">UseDeviceTsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">

		Sets or retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms690868(v=VS.85).aspx">UseDeviceTsid</a> property for a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>UseDeviceTsid</b> property is a Boolean value that indicates whether the fax server uses the device's TSID instead of a user-specified TSID.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

			You should not implement this interface. The Microsoft standard implementation provides complete functionality.
            

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>

			Use the <b>IFaxServer</b> interface to connect to and disconnect from an active fax server. Also use the interface to retrieve and set the properties of <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxServer</a> objects, and to create the objects listed in the following steps.
			

To connect to a fax server, and create other fax client objects, perform the following steps:

<ol>
<li>Call the <a href="https://msdn.microsoft.com/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve a pointer to an <b>IFaxServer</b> interface and create an instance of a <a href="https://msdn.microsoft.com/library/ms692367(v=VS.85).aspx">FaxServer</a> object. </li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">IFaxServer::Connect</a> method to initiate a connection with an active fax server. </li>
<li>After you obtain a connection, call the following methods to create the objects you need: 
<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/ms692836(v=VS.85).aspx">IFaxServer::GetJobs</a> method to create a <a href="https://msdn.microsoft.com/library/ms692796(v=VS.85).aspx">FaxJobs</a> object. Use this object to create <a href="https://msdn.microsoft.com/library/ms692342(v=VS.85).aspx">FaxJob</a> objects and enumerate the fax jobs associated with a connected fax server. </li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/ms692815(v=VS.85).aspx">IFaxServer::GetPorts</a> method to create a <a href="https://msdn.microsoft.com/library/ms692319(v=VS.85).aspx">FaxPorts</a> object. Use this object to create <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> objects and enumerate fax port configuration information for a connection to a fax server. </li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/ms690786(v=VS.85).aspx">IFaxServer::CreateDocument</a> method to create a <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. Use this object to transmit a fax and to retrieve and set the properties of FaxDoc objects. </li>
</ul>
</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms691936(v=VS.85).aspx">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method for each object to allow the object to deallocate itself. Call the method again, if necessary, to destroy the <a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a> or the <a href="https://msdn.microsoft.com/library/ms692372(v=VS.85).aspx">IFaxJobs</a> interface pointers. </li>
</ol>
Note that a client application should not call the <a href="https://msdn.microsoft.com/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to create <a href="https://msdn.microsoft.com/library/ms692796(v=VS.85).aspx">FaxJobs</a>, <a href="https://msdn.microsoft.com/library/ms692319(v=VS.85).aspx">FaxPorts</a> or <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> objects, or objects derived from these objects. For more information about creating and deallocating fax client objects, see the steps that are listed with each individual interface topic and the hierarchical diagram included in <a href="https://msdn.microsoft.com/library/ms691502(v=VS.85).aspx">The Fax Client Object Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

