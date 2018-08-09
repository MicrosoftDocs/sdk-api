---
UID: NN:faxcom.IFaxRoutingMethod
title: IFaxRoutingMethod
author: windows-sdk-content
description: The IFaxRoutingMethod dual interface is used by a fax client application to retrieve fax routing configuration information for a fax port on a connected fax server.
old-location: fax\_mfax_ifaxroutingmethod.htm
old-project: Fax
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
 - IFaxRoutingMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod interface


## -description


The <b>IFaxRoutingMethod</b> dual interface is used by a fax client application to retrieve fax routing configuration information for a fax port on a connected fax server. A <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object is a collection of <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> objects. 

The <b>IFaxRoutingMethod</b> interface includes the following interface methods. 
			<ul>
<li>Property methods to retrieve, enable, or disable a fax routing method for a specific <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. (Fax routing methods are defined by fax routing extension DLLs.)</li>
<li>Property methods to retrieve attributes of a <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object, such as the name of the DLL that exports the routing method. Attributes also include the GUID and function name that uniquely identify the routing method, and the routing method's user-friendly name.</li>
</ul>


A routing method is an action that is performed each time a fax is received on a port. If fax reception is not enabled on a port, the fax service disregards the routing methods associated with the port. Only enabled routing methods are executed when a fax is received. 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxRoutingMethod</b> interface to enable or disable a fax routing method on a specific fax port, and to retrieve and set the properties of a <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object. There is one FaxRoutingMethod object for each routing method associated with the specified fax port. 

A client application should not call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve an <b>IFaxRoutingMethod</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object.
				<ol>
<li>Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to connect to an active fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">IFaxServer::GetPorts</a> method to create and initialize a <a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a> object for the connected fax server.</li>
<li>Call the <a href="https://msdn.microsoft.com/57736284-43f4-4ac3-bb43-313e6ee4ea44">IFaxPorts::get_Count</a> method and then the <a href="https://msdn.microsoft.com/c5819801-f213-42c9-b8d8-5eaf352c0361">IFaxPorts::get_Item</a> method to retrieve <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. (You can also call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a> interface pointer.)</li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call the <a href="https://msdn.microsoft.com/c180dbac-2aaa-4e8e-9b1f-b6314b47d229">IFaxPort::GetRoutingMethods</a> interface method, to retrieve an IDispatch interface pointer to a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object.</li>
<li>Call the <a href="https://msdn.microsoft.com/7bbcf3aa-7dba-4452-817c-bf21bc646790">IFaxRoutingMethods::get_Count</a> method and then the <a href="https://msdn.microsoft.com/403ba8dc-6faa-4067-b77a-9c451baa8a33">IFaxRoutingMethods::get_Item</a> method to retrieve <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointers for each child <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object.</li>
<li>Use the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to call <b>IFaxRoutingMethod</b> interface methods.</li>
<li>Call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method for each <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object to allow the object to deallocate itself. Also call IUnknown::Release for each <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object, and to destroy the <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> interface pointer.</li>
</ol>





## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

