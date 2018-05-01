---
UID: NN:faxcom.IFaxStatus
title: IFaxStatus
author: windows-driver-content
description: The FaxStatus dual interface is used by a fax client application to retrieve status information for a specific port on a connected fax server.
old-location: fax\_mfax_ifaxstatus.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0ckz.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxStatus, IFaxStatus interface [Fax Service], IFaxStatus interface [Fax Service], described, _mfax_ifaxstatus, fax._mfax_ifaxstatus, faxcom/IFaxStatus
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
-	IFaxStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus interface


## -description


The <b>FaxStatus</b> dual interface is used by a fax client application to retrieve status information for a specific port on a connected fax server. The <b>IFaxStatus</b> interface includes the following interface methods:
<ul>
<li>A method to update status information for a fax port. </li>
<li>Property methods to retrieve attributes of a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object, such as whether the parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> is currently sending or receiving a fax transmission. Attributes also include document and transmission data, sender and recipient names, and routing information. </li>
</ul>

The <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object should only be created by a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. 




You can use the FaxStatus object to provide real-time status information about a parent FaxPort object. Some data is available at all times for an active fax port; other data is relative to sending or receiving a fax and is only available at those times.

		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxStatus</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxStatus</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a5ce733f-c83c-4d68-a600-f3f55c2d7908">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a5ce733f-c83c-4d68-a600-f3f55c2d7908">Refresh</a> method updates <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object information for the associated parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object.

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

<a href="https://msdn.microsoft.com/library/windows/hardware/mt427295">Address</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/mt427295">Address</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Address</b> property is a null-terminated string that contains the destination of a fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/35bf5f3e-2cb3-4e7a-994a-18bc6eeb7584">CallerId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/35bf5f3e-2cb3-4e7a-994a-18bc6eeb7584">CallerId</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>CallerId</b> property is a string that identifies the calling device that sent an inbound fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922691">Csid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922691">Csid</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Csid</b> property is a string that contains CSID information, typically the fax number of the receiving device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a0916ecc-7800-4a13-bcc1-9212b07d35e3">CurrentPage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/a0916ecc-7800-4a13-bcc1-9212b07d35e3">CurrentPage</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>CurrentPage</b> property is a number that identifies the current page of an active outbound fax job on a specific port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Description</b> property is a null-terminated string that describes the current status of the specified port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dd6c8cce-b2fd-4c77-8e74-dc1d851c0de6">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/dd6c8cce-b2fd-4c77-8e74-dc1d851c0de6">DeviceId</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>DeviceId</b> property is a number representing the permanent line identifier for the fax port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>DeviceName</b> property is a null-terminated string that contains the user-friendly display name for the fax port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff541150">DocumentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/ff541150">DocumentName</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>DocumentName</b> property is a null-terminated string that contains the user-friendly name associated with an active fax document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ec9b9196-f937-4601-b7a8-d5f2a33b276e">DocumentSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/ec9b9196-f937-4601-b7a8-d5f2a33b276e">DocumentSize</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>DocumentSize</b> property is the size of the fax document associated with the active outbound job on a specific port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b9784976-9844-4937-86e5-979aec8ade72">ElapsedTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/b9784976-9844-4937-86e5-979aec8ade72">ElapsedTime</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>ElapsedTime</b> property is a number that represents the elapsed time for an active fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7dd672cb-e460-4594-8aff-67292d4b34e3">PageCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/7dd672cb-e460-4594-8aff-67292d4b34e3">PageCount</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>PageCount</b> property represents the total number of pages in an outbound fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e7a63893-d8df-4253-80b0-3faab13934fd">Receive</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/e7a63893-d8df-4253-80b0-3faab13934fd">Receive</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Receive</b> property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8d681d5a-0ca7-4c86-9a53-f26e666cb329">RecipientName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/8d681d5a-0ca7-4c86-9a53-f26e666cb329">RecipientName</a> property for a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient of an inbound fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b42288a3-5814-4325-b3f5-9b39fde82b2b">RoutingString</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/b42288a3-5814-4325-b3f5-9b39fde82b2b">RoutingString</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>RoutingString</b> property is a null-terminated string that contains routing information for inbound fax transmissions that is specific to a fax service provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/239b98c5-be46-4e54-83f7-eb7f6250fa57">Send</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/239b98c5-be46-4e54-83f7-eb7f6250fa57">Send</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Send</b> property is a Boolean value that indicates whether a specified fax port is currently sending a fax. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt764038">SenderName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/mt764038">SenderName</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the user who sent the fax transmission.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2093664f-de48-4f8e-a047-4696377c6fd6">StartTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/2093664f-de48-4f8e-a047-4696377c6fd6">StartTime</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>StartTime</b> property is a number that represents the starting time for an active fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/60b80302-271a-4e83-9a4a-a2c3f6f2d1b6">SubmittedTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/60b80302-271a-4e83-9a4a-a2c3f6f2d1b6">SubmittedTime</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>SubmittedTime</b> property is a number that represents the time the user submitted the active fax job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn997387">Tsid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/dn997387">Tsid</a> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Tsid</b> property is a null-terminated string that contains the TSID associated with the fax port.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

			You should not implement this interface. The Microsoft standard implementation provides complete functionality.
            

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>

			Use the <b>IFaxStatus</b> interface to update the status information for a specific fax port, and to retrieve the properties of a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object. 





A client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <b>IFaxStatus</b> interface pointer. Instead, the application must perform the following steps to create an instance of a FaxStatus object: 


<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface. </li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">IFaxServer::GetPorts</a> method to create and initialize a <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object for the connected fax server. </li>
<li>Call the <a href="https://msdn.microsoft.com/57736284-43f4-4ac3-bb43-313e6ee4ea44">IFaxPorts::get_Count</a> method and then the <a href="https://msdn.microsoft.com/c5819801-f213-42c9-b8d8-5eaf352c0361">IFaxPorts::get_Item</a> method to retrieve <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. (You can also call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a> interface pointer.) </li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call the <a href="https://msdn.microsoft.com/d55d5ca8-6dd7-43c9-aba3-b6ed9f9b7558">IFaxPort::GetStatus</a> interface method, to retrieve an IDispatch interface pointer to a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object. </li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call <b>IFaxStatus</b> interface methods. </li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server. </li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object to allow the object to deallocate itself. Also call IUnknown::Release once for each <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object, and again to destroy both the <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> and the parent <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface pointers. </li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

