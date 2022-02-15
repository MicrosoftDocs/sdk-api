---
UID: NN:faxcom.IFaxRoutingMethods
title: IFaxRoutingMethods (faxcom.h)
description: The IFaxRoutingMethods dual interface is used by a fax client application to access the FaxRoutingMethod objects derived from a FaxPort object.
helpviewer_keywords: ["IFaxRoutingMethods","IFaxRoutingMethods interface [Fax Service]","IFaxRoutingMethods interface [Fax Service]","described","_mfax_ifaxroutingmethods","fax._mfax_ifaxroutingmethods","faxcom/IFaxRoutingMethods"]
old-location: fax\_mfax_ifaxroutingmethods.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6smr.htm
ms.date: 12/05/2018
ms.keywords: IFaxRoutingMethods, IFaxRoutingMethods interface [Fax Service], IFaxRoutingMethods interface [Fax Service],described, _mfax_ifaxroutingmethods, fax._mfax_ifaxroutingmethods, faxcom/IFaxRoutingMethods
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
 - IFaxRoutingMethods
 - faxcom/IFaxRoutingMethods
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
 - IFaxRoutingMethods
---

# IFaxRoutingMethods interface


## -description

The <b>IFaxRoutingMethods</b> dual interface is used by a fax client application to access the <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> objects derived from a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. The interface enumerates fax routing information for a specific fax port.  

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethods">FaxRoutingMethods</a> object is a collection of <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> objects. 

The <b>IFaxRoutingMethods</b> interface includes methods that allow a fax client application to perform the following tasks. 
			<ul>
<li>Retrieve the number of fax routing methods associated with a fax port.</li>
<li>Create and retrieve <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a> interface pointers for <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> objects.</li>
</ul>

## -inheritance

The <b>IFaxRoutingMethods</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxRoutingMethods</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxRoutingMethods</b> interface to create and retrieve <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a> interface pointers to <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> objects. There is one FaxRoutingMethod object for each routing method associated with the specified fax port.  

To create an instance of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object, perform the following steps. Note that a fax client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a> interface pointer.  
				<ol>
<li>Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to a fax server.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-getroutingmethods-vb">IFaxPort::GetRoutingMethods</a> method to create and initialize a <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethods">FaxRoutingMethods</a> object for the fax port.</li>
<li>Call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxroutingmethods-get_count">IFaxRoutingMethods::get_Count</a> method and then the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxroutingmethods-get_item">IFaxRoutingMethods::get_Item</a> method to retrieve <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointers for each child <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object. (You can also call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a> interface pointer). </li>
<li>Use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a> interface methods.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each <a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> object to allow the object to deallocate itself, and again to destroy the <b>IFaxRoutingMethods</b> interface pointer.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
