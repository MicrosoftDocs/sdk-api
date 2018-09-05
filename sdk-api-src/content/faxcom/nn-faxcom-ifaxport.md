---
UID: NN:faxcom.IFaxPort
title: IFaxPort
author: windows-sdk-content
description: The IFaxPort dual interface is used by a fax client application to access configuration information for a fax port on a connected fax server.
old-location: fax\_mfax_ifaxport.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_21ys.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxPort, IFaxPort interface [Fax Service], IFaxPort interface [Fax Service],described, _mfax_ifaxport, fax._mfax_ifaxport, faxcom/IFaxPort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcom.h
req.include-header: 
req.redist: 
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
 - IFaxPort
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort interface


## -description


The <b>IFaxPort</b> dual interface is used by a fax client application to access configuration information for a fax port on a connected fax server. The <b>IFaxPort</b> interface includes the following methods.
<ul>
<li>Methods to create <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> objects and <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> objects. </li>
<li>Property methods to set and retrieve individual property values associated with a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object retrieved by the <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> interface. A <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object is a collection of FaxPort objects.</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxPort</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxPort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxPort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c180dbac-2aaa-4e8e-9b1f-b6314b47d229">GetRoutingMethods</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c180dbac-2aaa-4e8e-9b1f-b6314b47d229">IFaxPort::GetRoutingMethods</a> interface method creates a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object for the parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The FaxRoutingMethods object allows enumeration of the fax routing methods associated with a fax port. Fax routing methods are defined by a fax routing extension DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d55d5ca8-6dd7-43c9-aba3-b6ed9f9b7558">GetStatus</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d55d5ca8-6dd7-43c9-aba3-b6ed9f9b7558">IFaxPort::GetStatus</a> method creates a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object for the parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The FaxStatus object contains the current status of a fax port.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxPort</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b09b6e5f-fa1d-4d0b-8581-e0ba779b72bb">CanModify</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b09b6e5f-fa1d-4d0b-8581-e0ba779b72bb">IFaxPort::get_CanModify</a> property is a Boolean value that indicates whether the user has permission to modify configuration information for the fax port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f4625705-8bee-4c84-a643-60085fbf5102">Csid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f4625705-8bee-4c84-a643-60085fbf5102">IFaxPort::get_Csid</a> property is a null-terminated string that contains the CSID associated with the fax port.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6909e37a-0a6c-475f-ab41-c2e1817349f5">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6909e37a-0a6c-475f-ab41-c2e1817349f5">IFaxPort::get_DeviceId</a> property is a number representing the permanent line identifier for the fax port. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/245641d0-1449-46df-a83a-283871612e0e">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/245641d0-1449-46df-a83a-283871612e0e">IFaxPort::get_Name</a> property is a null-terminated string that contains the 
user-friendly display name for a fax port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5440d77d-0bd3-47ca-9a7f-0af71a981d96">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5440d77d-0bd3-47ca-9a7f-0af71a981d96">IFaxPort::get_Priority</a> property is a number representing the transmission priority designated for a specified fax port. Priority determines the relative order in which available fax devices send outgoing transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/56661368-e93b-40c4-8ba2-a4a00dade9df">Receive</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/56661368-e93b-40c4-8ba2-a4a00dade9df">IFaxPort::get_Receive</a> property is a Boolean value that indicates whether a specified fax port is enabled to receive faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4f701de2-3c8a-4dd8-96b3-6e33a1662de2">Rings</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4f701de2-3c8a-4dd8-96b3-6e33a1662de2">IFaxPort::get_Rings</a> property represents the number of rings an incoming fax call should wait before the fax port answers the call. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/16703a2b-8dc4-46df-b235-c3bbb41fe253">Send</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/16703a2b-8dc4-46df-b235-c3bbb41fe253">IFaxPort::get_Send</a> property is a Boolean value that indicates whether a fax port is enabled to send faxes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3449c761-9d36-407f-8434-3957f2ab1dd1">Tsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3449c761-9d36-407f-8434-3957f2ab1dd1">IFaxPort::get_Tsid</a> property is a null-terminated string that contains the TSID associated with the fax port.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  A fax client application can call the <a href="https://msdn.microsoft.com/b09b6e5f-fa1d-4d0b-8581-e0ba779b72bb">IFaxPort::get_CanModify</a> property before calling any method that begins with <b>IFaxPort::put_</b> to ensure that the client has access to modify the specified fax port.</div>
<div> </div>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxPort</b> interface to retrieve and set the properties of a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. 

A client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <b>IFaxPort</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. 
				<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to connect to an active fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">IFaxServer::GetPorts</a> method to create and initialize a <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object for the connected fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/57736284-43f4-4ac3-bb43-313e6ee4ea44">IFaxPorts::get_Count</a> method and then the <a href="https://msdn.microsoft.com/c5819801-f213-42c9-b8d8-5eaf352c0361">IFaxPorts::get_Item</a> method to retrieve <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. (You can also call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxPort</b> interface pointer.)</li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call <b>IFaxPort</b> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object to allow the object to deallocate itself, and again to destroy the <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

