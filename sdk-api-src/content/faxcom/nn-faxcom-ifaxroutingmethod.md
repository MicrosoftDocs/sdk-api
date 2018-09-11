---
UID: NN:faxcom.IFaxRoutingMethod
title: IFaxRoutingMethod
author: windows-sdk-content
description: The IFaxRoutingMethod dual interface is used by a fax client application to retrieve fax routing configuration information for a fax port on a connected fax server.
old-location: fax\_mfax_ifaxroutingmethod.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4skk.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxRoutingMethod, IFaxRoutingMethod interface [Fax Service], IFaxRoutingMethod interface [Fax Service],described, _mfax_ifaxroutingmethod, fax._mfax_ifaxroutingmethod, faxcom/IFaxRoutingMethod
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
 - IFaxRoutingMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod interface


## -description


The <b>IFaxRoutingMethod</b> dual interface is used by a fax client application to retrieve fax routing configuration information for a fax port on a connected fax server. A <a href="https://msdn.microsoft.com/en-us/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object is a collection of <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> objects. 

The <b>IFaxRoutingMethod</b> interface includes the following interface methods. 
			<ul>
<li>Property methods to retrieve, enable, or disable a fax routing method for a specific <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. (Fax routing methods are defined by fax routing extension DLLs.)</li>
<li>Property methods to retrieve attributes of a <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> object, such as the name of the DLL that exports the routing method. Attributes also include the GUID and function name that uniquely identify the routing method, and the routing method's user-friendly name.</li>
</ul>


A routing method is an action that is performed each time a fax is received on a port. If fax reception is not enabled on a port, the fax service disregards the routing methods associated with the port. Only enabled routing methods are executed when a fax is received. 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxRoutingMethod</b> interface to enable or disable a fax routing method on a specific fax port, and to retrieve and set the properties of a <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> object. There is one FaxRoutingMethod object for each routing method associated with the specified fax port. 

A client application should not call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve an <b>IFaxRoutingMethod</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> object.
				<ol>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692315(v=VS.85).aspx">IFaxServer::Connect</a> method to connect to an active fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692815(v=VS.85).aspx">IFaxServer::GetPorts</a> method to create and initialize a <a href="https://msdn.microsoft.com/en-us/library/ms692319(v=VS.85).aspx">FaxPorts</a> object for the connected fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms692338(v=VS.85).aspx">IFaxPorts::get_Count</a> method and then the <a href="https://msdn.microsoft.com/en-us/library/ms690813(v=VS.85).aspx">IFaxPorts::get_Item</a> method to retrieve <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. (You can also call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a> interface pointer.)</li>
<li>Use the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to call the <a href="https://msdn.microsoft.com/en-us/library/ms691943(v=VS.85).aspx">IFaxPort::GetRoutingMethods</a> interface method, to retrieve an IDispatch interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms690829(v=VS.85).aspx">IFaxRoutingMethods::get_Count</a> method and then the <a href="https://msdn.microsoft.com/en-us/library/ms692331(v=VS.85).aspx">IFaxRoutingMethods::get_Item</a> method to retrieve <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> object.</li>
<li>Use the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to call <b>IFaxRoutingMethod</b> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms691936(v=VS.85).aspx">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> object to allow the object to deallocate itself. Also call IUnknown::Release for each <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object, and to destroy the <a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

