---
UID: NN:faxcom.IFaxStatus
title: IFaxStatus (faxcom.h)
description: The FaxStatus dual interface is used by a fax client application to retrieve status information for a specific port on a connected fax server.
helpviewer_keywords: ["IFaxStatus","IFaxStatus interface [Fax Service]","IFaxStatus interface [Fax Service]","described","_mfax_ifaxstatus","fax._mfax_ifaxstatus","faxcom/IFaxStatus"]
old-location: fax\_mfax_ifaxstatus.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0ckz.htm
ms.date: 12/05/2018
ms.keywords: IFaxStatus, IFaxStatus interface [Fax Service], IFaxStatus interface [Fax Service],described, _mfax_ifaxstatus, fax._mfax_ifaxstatus, faxcom/IFaxStatus
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
 - IFaxStatus
 - faxcom/IFaxStatus
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
 - IFaxStatus
---

# IFaxStatus interface


## -description

The <b>FaxStatus</b> dual interface is used by a fax client application to retrieve status information for a specific port on a connected fax server. The <b>IFaxStatus</b> interface includes the following interface methods:
<ul>
<li>A method to update status information for a fax port. </li>
<li>Property methods to retrieve attributes of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object, such as whether the parent <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> is currently sending or receiving a fax transmission. Attributes also include document and transmission data, sender and recipient names, and routing information. </li>
</ul>

The <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object should only be created by a <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. 




You can use the FaxStatus object to provide real-time status information about a parent FaxPort object. Some data is available at all times for an active fax port; other data is relative to sending or receiving a fax and is only available at those times.

## -inheritance

The <b>IFaxStatus</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxStatus</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You should not implement this interface. The Microsoft standard implementation provides complete functionality.
            

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the <b>IFaxStatus</b> interface to update the status information for a specific fax port, and to retrieve the properties of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. 





A client application should not call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve an <b>IFaxStatus</b> interface pointer. Instead, the application must perform the following steps to create an instance of a FaxStatus object: 


<ol>
<li>Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function to retrieve a pointer to an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface. </li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method to connect to an active fax server. </li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-getports-vb">IFaxServer::GetPorts</a> method to create and initialize a <a href="/previous-versions/windows/desktop/fax/-mfax-faxports">FaxPorts</a> object for the connected fax server. </li>
<li>Call the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_count">IFaxPorts::get_Count</a> method and then the <a href="/previous-versions/windows/desktop/api/faxcom/nf-faxcom-ifaxports-get_item">IFaxPorts::get_Item</a> method to retrieve <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointers for each child <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object. (You can also call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to retrieve an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a> interface pointer.) </li>
<li>Use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-getstatus-vb">IFaxPort::GetStatus</a> interface method, to retrieve an IDispatch interface pointer to a <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object. </li>
<li>Use the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to call <b>IFaxStatus</b> interface methods. </li>
<li>Call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server. </li>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for each <a href="/previous-versions/windows/desktop/fax/-mfax-faxstatus">FaxStatus</a> object to allow the object to deallocate itself. Also call IUnknown::Release once for each <a href="/previous-versions/windows/desktop/fax/-mfax-faxport">FaxPort</a> object, and again to destroy both the <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a> and the parent <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a> interface pointers. </li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
