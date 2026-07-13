---
UID: NN:faxcom.IFaxJobs
title: IFaxJobs (faxcom.h)
description: The IFaxJobs dual interface is used by a fax client application to access the FaxJob objects derived from a FaxServer object. The interface enumerates the fax jobs associated with a connected fax server.
helpviewer_keywords: ["IFaxJobs","IFaxJobs interface [Fax Service]","IFaxJobs interface [Fax Service]","described","_mfax_ifaxjobs","fax._mfax_ifaxjobs","faxcom/IFaxJobs"]
old-location: fax\_mfax_ifaxjobs.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8bjn.htm
ms.date: 12/05/2018
ms.keywords: IFaxJobs, IFaxJobs interface [Fax Service], IFaxJobs interface [Fax Service],described, _mfax_ifaxjobs, fax._mfax_ifaxjobs, faxcom/IFaxJobs
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
 - IFaxJobs
 - faxcom/IFaxJobs
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
 - IFaxJobs
---

# IFaxJobs interface


## -description

The <b>IFaxJobs</b> dual interface is used by a fax client application to access the <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> objects derived from a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a> object. The interface enumerates the fax jobs associated with a connected fax server.

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs">FaxJobs</a> object is a collection of <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> objects.

The <b>IFaxJobs</b> interface includes methods that allow a fax client application to perform the following tasks. 
			<ul>
<li>Retrieve the number of fax jobs associated with a connected fax server.</li>
<li>Create and retrieve IFaxJob interface pointers for FaxJob objects.</li>
</ul>

## -inheritance

The <b>IFaxJobs</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxJobs</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxJobs</b> interface to create and retrieve <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a> interface pointers to <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> objects. There is one FaxJob object for each queued job associated with the connected fax server. 

To create an instance of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> object, perform the following steps. Note that a fax client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a> interface pointer. 
				<ol>
<li>Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an IFaxServer interface.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to a fax server.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getjobs-vb">IFaxServer::GetJobs</a> method to create and initialize a <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs">FaxJobs</a> object for the fax server.</li>
<li>Call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxjobs-get_count">IFaxJobs::get_Count</a> method and then the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxjobs-get_item">IFaxJobs::get_Item</a> method to retrieve <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointers for each child <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> object.</li>
<li>Use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjob">IFaxJob</a> interface methods. (You can also call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxJob</b> interface pointer.)</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> object to allow the object to deallocate itself, and again to destroy the <b>IFaxJobs</b> interface pointer.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
