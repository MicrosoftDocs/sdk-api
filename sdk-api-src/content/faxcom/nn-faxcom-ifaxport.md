---
UID: NN:faxcom.IFaxPort
title: IFaxPort (faxcom.h)
description: The IFaxPort dual interface is used by a fax client application to access configuration information for a fax port on a connected fax server.
helpviewer_keywords: ["IFaxPort","IFaxPort interface [Fax Service]","IFaxPort interface [Fax Service]","described","_mfax_ifaxport","fax._mfax_ifaxport","faxcom/IFaxPort"]
old-location: fax\_mfax_ifaxport.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_21ys.htm
ms.date: 12/05/2018
ms.keywords: IFaxPort, IFaxPort interface [Fax Service], IFaxPort interface [Fax Service],described, _mfax_ifaxport, fax._mfax_ifaxport, faxcom/IFaxPort
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
 - IFaxPort
 - faxcom/IFaxPort
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
 - IFaxPort
---

# IFaxPort interface


## -description

The <b>IFaxPort</b> dual interface is used by a fax client application to access configuration information for a fax port on a connected fax server. The <b>IFaxPort</b> interface includes the following methods.
<ul>
<li>Methods to create <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethods">FaxRoutingMethods</a> objects and <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> objects. </li>
<li>Property methods to set and retrieve individual property values associated with a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object retrieved by the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> interface. A <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object is a collection of FaxPort objects.</li>
</ul>

## -inheritance

The <b>IFaxPort</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxPort</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  A fax client application can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-get-canmodify-vb">IFaxPort::get_CanModify</a> property before calling any method that begins with <b>IFaxPort::put_</b> to ensure that the client has access to modify the specified fax port.</div>
<div> </div>
<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxPort</b> interface to retrieve and set the properties of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. 

A client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <b>IFaxPort</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. 
				<ol>
<li>Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to an active fax server.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">IFaxServer::GetPorts</a> method to create and initialize a <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object for the connected fax server.</li>
<li>Call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_count">IFaxPorts::get_Count</a> method and then the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_item">IFaxPorts::get_Item</a> method to retrieve <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointers for each child <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. (You can also call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxPort</b> interface pointer.)</li>
<li>Use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call <b>IFaxPort</b> interface methods.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object to allow the object to deallocate itself, and again to destroy the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> interface pointer.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
