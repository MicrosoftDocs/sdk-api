---
UID: NN:faxcom.IFaxRoutingMethod
title: IFaxRoutingMethod (faxcom.h)
description: The IFaxRoutingMethod dual interface is used by a fax client application to retrieve fax routing configuration information for a fax port on a connected fax server.
helpviewer_keywords: ["IFaxRoutingMethod","IFaxRoutingMethod interface [Fax Service]","IFaxRoutingMethod interface [Fax Service]","described","_mfax_ifaxroutingmethod","fax._mfax_ifaxroutingmethod","faxcom/IFaxRoutingMethod"]
old-location: fax\_mfax_ifaxroutingmethod.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4skk.htm
ms.date: 12/05/2018
ms.keywords: IFaxRoutingMethod, IFaxRoutingMethod interface [Fax Service], IFaxRoutingMethod interface [Fax Service],described, _mfax_ifaxroutingmethod, fax._mfax_ifaxroutingmethod, faxcom/IFaxRoutingMethod
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
 - IFaxRoutingMethod
 - faxcom/IFaxRoutingMethod
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
 - IFaxRoutingMethod
---

# IFaxRoutingMethod interface


## -description

The <b>IFaxRoutingMethod</b> dual interface is used by a fax client application to retrieve fax routing configuration information for a fax port on a connected fax server. A <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethods">FaxRoutingMethods</a> object is a collection of <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> objects. 

The <b>IFaxRoutingMethod</b> interface includes the following interface methods. 
			<ul>
<li>Property methods to retrieve, enable, or disable a fax routing method for a specific <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. (Fax routing methods are defined by fax routing extension DLLs.)</li>
<li>Property methods to retrieve attributes of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object, such as the name of the DLL that exports the routing method. Attributes also include the GUID and function name that uniquely identify the routing method, and the routing method's user-friendly name.</li>
</ul>


A routing method is an action that is performed each time a fax is received on a port. If fax reception is not enabled on a port, the fax service disregards the routing methods associated with the port. Only enabled routing methods are executed when a fax is received.

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxRoutingMethod</b> interface to enable or disable a fax routing method on a specific fax port, and to retrieve and set the properties of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object. There is one FaxRoutingMethod object for each routing method associated with the specified fax port. 

A client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <b>IFaxRoutingMethod</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object.
				<ol>
<li>Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to an active fax server.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">IFaxServer::GetPorts</a> method to create and initialize a <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object for the connected fax server.</li>
<li>Call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_count">IFaxPorts::get_Count</a> method and then the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_item">IFaxPorts::get_Item</a> method to retrieve <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointers for each child <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. (You can also call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a> interface pointer.)</li>
<li>Use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-getroutingmethods-vb">IFaxPort::GetRoutingMethods</a> interface method, to retrieve an IDispatch interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethods">FaxRoutingMethods</a> object.</li>
<li>Call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxroutingmethods-get_count">IFaxRoutingMethods::get_Count</a> method and then the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxroutingmethods-get_item">IFaxRoutingMethods::get_Item</a> method to retrieve <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointers for each child <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object.</li>
<li>Use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call <b>IFaxRoutingMethod</b> interface methods.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object to allow the object to deallocate itself. Also call IUnknown::Release for each <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object, and to destroy the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> interface pointer.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>