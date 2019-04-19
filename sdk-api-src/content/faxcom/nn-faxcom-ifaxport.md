---
UID: NN:faxcom.IFaxPort
title: IFaxPort (faxcom.h)
author: windows-sdk-content
description: The IFaxPort dual interface is used by a fax client application to access configuration information for a fax port on a connected fax server.
old-location: fax\_mfax_ifaxport.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_21ys.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxPort, IFaxPort interface [Fax Service], IFaxPort interface [Fax Service],described, _mfax_ifaxport, fax._mfax_ifaxport, faxcom/IFaxPort
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
 - IFaxPort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxPort interface


## -description


The <b>IFaxPort</b> dual interface is used by a fax client application to access configuration information for a fax port on a connected fax server. The <b>IFaxPort</b> interface includes the following methods.
<ul>
<li>Methods to create <a href="https://msdn.microsoft.com/en-us/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> objects and <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> objects. </li>
<li>Property methods to set and retrieve individual property values associated with a <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object retrieved by the <a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a> interface. A <a href="https://msdn.microsoft.com/en-us/library/ms692319(v=VS.85).aspx">FaxPorts</a> object is a collection of FaxPort objects.</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxPort</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxPort</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms691943(v=VS.85).aspx">GetRoutingMethods</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691943(v=VS.85).aspx">IFaxPort::GetRoutingMethods</a> interface method creates a <a href="https://msdn.microsoft.com/en-us/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object for the parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The FaxRoutingMethods object allows enumeration of the fax routing methods associated with a fax port. Fax routing methods are defined by a fax routing extension DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms692788(v=VS.85).aspx">GetStatus</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692788(v=VS.85).aspx">IFaxPort::GetStatus</a> method creates a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object for the parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The FaxStatus object contains the current status of a fax port.

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

<a href="https://msdn.microsoft.com/en-us/library/ms692798(v=VS.85).aspx">CanModify</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692798(v=VS.85).aspx">IFaxPort::get_CanModify</a> property is a Boolean value that indicates whether the user has permission to modify configuration information for the fax port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690876(v=VS.85).aspx">Csid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690876(v=VS.85).aspx">IFaxPort::get_Csid</a> property is a null-terminated string that contains the CSID associated with the fax port.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692379(v=VS.85).aspx">DeviceId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692379(v=VS.85).aspx">IFaxPort::get_DeviceId</a> property is a number representing the permanent line identifier for the fax port. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690887(v=VS.85).aspx">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690887(v=VS.85).aspx">IFaxPort::get_Name</a> property is a null-terminated string that contains the 
user-friendly display name for a fax port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms690737(v=VS.85).aspx">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690737(v=VS.85).aspx">IFaxPort::get_Priority</a> property is a number representing the transmission priority designated for a specified fax port. Priority determines the relative order in which available fax devices send outgoing transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692368(v=VS.85).aspx">Receive</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692368(v=VS.85).aspx">IFaxPort::get_Receive</a> property is a Boolean value that indicates whether a specified fax port is enabled to receive faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms691443(v=VS.85).aspx">Rings</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms691443(v=VS.85).aspx">IFaxPort::get_Rings</a> property represents the number of rings an incoming fax call should wait before the fax port answers the call. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692839(v=VS.85).aspx">Send</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692839(v=VS.85).aspx">IFaxPort::get_Send</a> property is a Boolean value that indicates whether a fax port is enabled to send faxes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms692284(v=VS.85).aspx">Tsid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms692284(v=VS.85).aspx">IFaxPort::get_Tsid</a> property is a null-terminated string that contains the TSID associated with the fax port.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  A fax client application can call the <a href="https://msdn.microsoft.com/en-us/library/ms692798(v=VS.85).aspx">IFaxPort::get_CanModify</a> property before calling any method that begins with <b>IFaxPort::put_</b> to ensure that the client has access to modify the specified fax port.</div>
<div> </div>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxPort</b> interface to retrieve and set the properties of a <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. 

A client application should not call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve an <b>IFaxPort</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. 
				<ol>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">IFaxServer::Connect</a> method to connect to an active fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692815(v=VS.85).aspx">IFaxServer::GetPorts</a> method to create and initialize a <a href="https://msdn.microsoft.com/en-us/library/ms692319(v=VS.85).aspx">FaxPorts</a> object for the connected fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692338(v=VS.85).aspx">IFaxPorts::get_Count</a> method and then the <a href="https://msdn.microsoft.com/en-us/library/ms690813(v=VS.85).aspx">IFaxPorts::get_Item</a> method to retrieve <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. (You can also call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxPort</b> interface pointer.)</li>
<li>Use the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to call <b>IFaxPort</b> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms691936(v=VS.85).aspx">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object to allow the object to deallocate itself, and again to destroy the <a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

