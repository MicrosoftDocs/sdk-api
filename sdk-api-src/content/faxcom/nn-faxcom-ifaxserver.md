---
UID: NN:faxcom.IFaxServer
title: IFaxServer
author: windows-driver-content
description: The IFaxServer dual interface is used by a fax client application to manage a connection to the fax service.
old-location: fax\_mfax_ifaxserver_client.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8dx0.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: IFaxServer, IFaxServer interface [Fax Service], IFaxServer interface [Fax Service], described, _mfax_ifaxserver_client, fax._mfax_ifaxserver_client, faxcom/IFaxServer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	IFaxServer
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer interface


## -description


The <b>IFaxServer</b> dual interface is used by a fax client application to manage a connection to the fax service. The interface retrieves and sets information about <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> objects; for example, settings for retransmission, branding, archiving and cover pages; discount rate periods; and the status of the fax server queue. The <b>IFaxServer</b> interface includes the following methods:
<ul>
<li>Methods to initiate and terminate connections with a fax server.</li>
<li>Property methods to retrieve and set individual property values of <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> objects. </li>
<li>Methods to create <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a>, <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> and <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> objects. </li>
</ul><div class="alert"><b>Note</b>  A fax client application must call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to initiate a connection with an active fax server before accessing most interfaces that begin with <b>IFax</b>. (A fax server connection is not required to access an <a href="https://msdn.microsoft.com/a4c46893-502d-4d5c-a895-837cffc014e4">IFaxTiff</a> interface.)</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServer</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxServer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">Connect</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">Connect</a> method connects a fax client application to the specified fax server. Before accessing most interfaces that begin with <b>IFax</b>, the application must call this method to initiate a connection with an active fax server. A fax server connection is not required to access an <a href="https://msdn.microsoft.com/a4c46893-502d-4d5c-a895-837cffc014e4">IFaxTiff</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5132538b-8250-4279-8091-19f112176594">CreateDocument</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5132538b-8250-4279-8091-19f112176594">IFaxServer::CreateDocument</a> method creates a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object for a specified <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The FaxDoc object allows a user to create and transmit a document to one or more fax recipients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">Disconnect</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method terminates a fax client application's connection to a fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45b195f9-0ac9-4150-84cf-64049cc4053f">GetJobs</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/45b195f9-0ac9-4150-84cf-64049cc4053f">GetJobs</a> method creates and initializes a <a href="https://msdn.microsoft.com/9df2f27f-b0a6-4ba5-920b-320dd83f6e40">FaxJobs</a> object for a specified <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object allows enumeration of the current queued jobs for the connected fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">GetPorts</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">GetPorts</a> method creates and initializes a <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object for a specified <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The FaxPorts object allows enumeration of fax port configuration information for the connected fax server.

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

<a href="https://msdn.microsoft.com/1c266ddb-62dc-4faf-9761-1c8c08c0b125">ArchiveDirectory</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1c266ddb-62dc-4faf-9761-1c8c08c0b125">IFaxServer::get_ArchiveDirectory</a> method retrieves the <b>ArchiveDirectory</b> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>ArchiveDirectory</b> property is a null-terminated string that contains the location in which the fax server stores archived outbound faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8cf29336-f41d-4357-a6ea-c0b8ca3344ba">ArchiveOutboundFaxes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/8cf29336-f41d-4357-a6ea-c0b8ca3344ba">ArchiveOutboundFaxes</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>ArchiveOutboundFaxes</b> property is a Boolean value that indicates whether the fax server archives outgoing fax transmissions. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9e5f913a-b526-4ea9-9929-92062d2339bc">Branding</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/9e5f913a-b526-4ea9-9929-92062d2339bc">Branding</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>Branding</b> property is a Boolean value that indicates whether the fax server generates branding information at the top of fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a13c189-0a35-4bb1-bae1-8c24784d9bbb">DirtyDays</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/8a13c189-0a35-4bb1-bae1-8c24784d9bbb">DirtyDays</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>DirtyDays</b> property is the number of days the fax server retains an unsent job in the fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/959f2960-2e42-485e-9791-53849166bf88">DiscountRateEndHour</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/959f2960-2e42-485e-9791-53849166bf88">DiscountRateEndHour</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>DiscountRateEndHour</b> property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a8e1bf04-7fc4-48b3-8682-b06c550122a7">DiscountRateEndMinute</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">

		Sets or retrieves the <a href="https://msdn.microsoft.com/a8e1bf04-7fc4-48b3-8682-b06c550122a7">DiscountRateEndMinute</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>DiscountRateEndMinute</b> property is a number that represents the minute the discount period ends. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b144d4db-bd0e-4198-8653-6b22013c3d2e">DiscountRateStartHour</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">

		Sets or retrieves the <a href="https://msdn.microsoft.com/b144d4db-bd0e-4198-8653-6b22013c3d2e">DiscountRateStartHour</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>DiscountRateStartHour</b> property is a number that represents the hour the discount period begins. The discount period applies only to outgoing fax transmissions. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/98355801-ad54-4b1e-a2f2-dcd22ede26e2">DiscountRateStartMinute</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/98355801-ad54-4b1e-a2f2-dcd22ede26e2">DiscountRateStartMinute</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>DiscountRateStartMinute</b> property is a number that represents the minute the discount period begins. The discount period applies only to outgoing fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/36b39388-38c5-46f4-a5d4-888240f50ef3">PauseServerQueue</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/36b39388-38c5-46f4-a5d4-888240f50ef3">PauseServerQueue</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>PauseServerQueue</b> property is a Boolean value that indicates whether the fax server has paused the fax job queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7766f135-24b3-4995-ad07-f69dcf4e396a">Retries</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/7766f135-24b3-4995-ad07-f69dcf4e396a">Retries</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>Retries</b> property is a value that represents the number of times the fax server attempts to retransmit an outgoing fax when the initial transmission fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/03806cfe-99e4-4559-a651-1195094e4f8b">RetryDelay</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/03806cfe-99e4-4559-a651-1195094e4f8b">RetryDelay</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>RetryDelay</b> property is a value that represents the time interval, in minutes, the fax server waits before attempting to retransmit an outbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/889e7233-fe5b-41f9-8436-0c7b28d78653">ServerCoverpage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/889e7233-fe5b-41f9-8436-0c7b28d78653">ServerCoverpage</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>ServerCoverpage</b> property is a Boolean value that indicates whether the fax server permits the use of common cover pages only. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7787fa4c-32fc-4f30-abda-31f9b30092c3">ServerMapiProfile</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the <a href="https://msdn.microsoft.com/7787fa4c-32fc-4f30-abda-31f9b30092c3">ServerMapiProfile</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>ServerMapiProfile</b> property is a null-terminated string that contains the MAPI user profile that the fax server uses for routing incoming fax transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a27d55e8-68c0-4700-becb-d56ecddbef44">UseDeviceTsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">

		Sets or retrieves the <a href="https://msdn.microsoft.com/a27d55e8-68c0-4700-becb-d56ecddbef44">UseDeviceTsid</a> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>UseDeviceTsid</b> property is a Boolean value that indicates whether the fax server uses the device's TSID instead of a user-specified TSID.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

			You should not implement this interface. The Microsoft standard implementation provides complete functionality.
            

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>

			Use the <b>IFaxServer</b> interface to connect to and disconnect from an active fax server. Also use the interface to retrieve and set the properties of <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxServer</a> objects, and to create the objects listed in the following steps.
			

To connect to a fax server, and create other fax client objects, perform the following steps:

<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <b>IFaxServer</b> interface and create an instance of a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. </li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to initiate a connection with an active fax server. </li>
<li>After you obtain a connection, call the following methods to create the objects you need: 
<ul>
<li>The <a href="https://msdn.microsoft.com/45b195f9-0ac9-4150-84cf-64049cc4053f">IFaxServer::GetJobs</a> method to create a <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a> object. Use this object to create <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> objects and enumerate the fax jobs associated with a connected fax server. </li>
<li>The <a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">IFaxServer::GetPorts</a> method to create a <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object. Use this object to create <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> objects and enumerate fax port configuration information for a connection to a fax server. </li>
<li>The <a href="https://msdn.microsoft.com/5132538b-8250-4279-8091-19f112176594">IFaxServer::CreateDocument</a> method to create a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. Use this object to transmit a fax and to retrieve and set the properties of FaxDoc objects. </li>
</ul>
</li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method for each object to allow the object to deallocate itself. Call the method again, if necessary, to destroy the <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> or the <a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a> interface pointers. </li>
</ol>
Note that a client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to create <a href="https://msdn.microsoft.com/7a8ad6e7-8db6-49ba-98de-da583907a54e">FaxJobs</a>, <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> or <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> objects, or objects derived from these objects. For more information about creating and deallocating fax client objects, see the steps that are listed with each individual interface topic and the hierarchical diagram included in <a href="https://msdn.microsoft.com/f8d9f711-c9b3-4ff2-8a27-13ff43094e61">The Fax Client Object Model</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

