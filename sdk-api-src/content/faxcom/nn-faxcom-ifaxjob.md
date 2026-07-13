---
UID: NN:faxcom.IFaxJob
title: IFaxJob (faxcom.h)
description: The IFaxJob dual interface is used by a fax client application to access information for a fax job on a connected fax server. A FaxJobs object is a collection of FaxJob objects.
helpviewer_keywords: ["IFaxJob","IFaxJob interface [Fax Service]","IFaxJob interface [Fax Service]","described","_mfax_ifaxjob","fax._mfax_ifaxjob","faxcom/IFaxJob"]
old-location: fax\_mfax_ifaxjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_75sy.htm
ms.date: 12/05/2018
ms.keywords: IFaxJob, IFaxJob interface [Fax Service], IFaxJob interface [Fax Service],described, _mfax_ifaxjob, fax._mfax_ifaxjob, faxcom/IFaxJob
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
 - IFaxJob
 - faxcom/IFaxJob
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
 - IFaxJob
---

# IFaxJob interface


## -description

The <b>IFaxJob</b> dual interface is used by a fax client application to access information for a fax job on a connected fax server. A <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs">FaxJobs</a> object is a collection of <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> objects.

The IFaxJob interface includes the following methods.
			<ul>
<li>A method to modify the job queue status of a fax job.</li>
<li>A method to refresh FaxJob object information.</li>
<li>Property methods to retrieve individual property values associated with a FaxJob object retrieved by the IFaxJobs interface.</li>
</ul>

## -inheritance

The <b>IFaxJob</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxJob</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality. 

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxJob</b> interface to access the job status for incoming and outgoing fax transmissions, and to pause, resume, cancel or restart a fax job. You can also use the interface to retrieve the properties of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> object.

A client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <b>IFaxJob</b> interface pointer. Instead, the application must perform the following steps to create an instance of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> object. 
				<ol>
<li>Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getjobs-vb">IFaxServer::GetJobs</a> method to create and initialize a <a href="/previous-versions/windows/desktop/fax/-mfax-faxjobs">FaxJobs</a> object for the connected fax server.</li>
<li>Call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxjobs-get_count">IFaxJobs::get_Count</a> method and then the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxjobs-get_item">IFaxJobs::get_Item</a> method to retrieve <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointers for each child <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> object. (You can also call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxJob</b> interface pointer.)</li>
<li>Use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call <b>IFaxJob</b> interface methods.</li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.</li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each <a href="/previous-versions/windows/desktop/fax/-mfax-faxjob">FaxJob</a> object to allow the object to deallocate itself, and again to destroy the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxjobs">IFaxJobs</a> interface pointer.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
